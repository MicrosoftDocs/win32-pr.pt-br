---
description: Os dispositivos portáteis do Windows oferecem suporte às seguintes propriedades de áudio.
ms.assetid: 5d6c6a95-abb7-4191-a961-bcb30ca96bb6
title: Propriedades de áudio (PortableDevice. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Audio
api_type:
- HeaderDef
api_location:
- PortableDevice.h
ms.openlocfilehash: 1bdab201fc987d5bc1aff3638fbb57358115fdce
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105781203"
---
# <a name="audio-properties"></a>Propriedades de áudio

Os dispositivos portáteis do Windows oferecem suporte às seguintes propriedades de áudio.



| Propriedade                         | VarType     | Descrição                                                                                                                                                                                                        |
|----------------------------------|-------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **\_profundidade de \_ bit de áudio WPD \_**       | **\_UI4 VT** | A profundidade de bits do áudio.                                                                                                                                                                                        |
| **taxa de bits de \_ áudio WPD \_**          | **\_UI4 VT** | A taxa de bits do áudio, em bits por segundo.                                                                                                                                                                     |
| **\_alinhamento de \_ bloco de áudio WPD \_** | **\_UI4 VT** | O alinhamento de bloco do arquivo de áudio, em bytes.                                                                                                                                                                   |
| **\_contagem de \_ canais de áudio WPD \_**   | **VT \_ R4**  | O número de canais neste arquivo de áudio, por exemplo, 1, 2 ou 5,1.                                                                                                                                              |
| **\_código de \_ formato de áudio WPD \_**     | **\_UI4 VT** | O número de código do formato WAVE registrado. Para obter uma lista de formatos de onda registrados, confira o artigo [códigos FOURCC registrados e formatos de onda](https://msdn2.microsoft.com/library/ms867195.aspx) no site do MSDN. |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------|---------------------------------------------------------------------------------------------|
| parâmetro<br/> | <dl> <dt>PortableDevice. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Propriedades e atributos WPD**](properties-and-attributes.md)
</dt> </dl>

 

 




