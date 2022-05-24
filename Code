import sounddevice as sd
import numpy as np

duration = 0.3  # длительность сигнала в секундах
amplitude = 0.5  # амплитуда  (в пределах: +-1.0)
frequency = 293.6648  # частота сигнала в [Гц]
# т.к. невозможно программно организовать аналоговый сигнал, необходимо обозначить
fs = 80000 # 80 тыс. временных отсчетов в 1 секунду количество временных отчетов, т.е. частоту дискретизации (об этом чуть позже)

timeSamples = np.arange(np.ceil(duration * fs)) / fs

signal2 = amplitude * np.sin(2 * np.pi * 986 * timeSamples)
signal3 = amplitude * np.sin(2 * np.pi * 1046 * timeSamples)
signal4 = amplitude * np.sin(2 * np.pi * 1174 * timeSamples)
signal5 = amplitude * np.sin(2 * np.pi * 1318 * timeSamples)
signalSumm = signal2 + signal3 + signal4 + signal5

sum = []
sum = np.concatenate((signal3,signal2,signal3,signal4,signal5,signal4,signal5,signal3,signal4,signal5), axis=0, out=None, dtype=None, casting="same_kind")
sd.play(sum, fs, None, 1)
