```

from abc import ABC, abstractmethod
from dataclasses import dataclass


class Human(ABC):
    @abstractmethod
    def say_hello(self):
        pass


@dataclass
class InformationMixin:
    full_name: str
    location: str
    language: str


@dataclass
class Developer(Human, InformationMixin):

    def say_hello(self):
        print('Glad to see you here.')      
        

sty = Developer('Seyed-Taher-Yaghoubi', 'Iran','Tehran' ,'Persian')   
sty.say_hello()

```
