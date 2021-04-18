---
description: Os dispositivos portáteis do Windows oferecem suporte às seguintes propriedades de vídeo.
ms.assetid: e6df5b2d-ceb8-4de0-b60b-9102c77143fe
title: Propriedades do vídeo (PortableDevice. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Video
api_type:
- HeaderDef
api_location:
- PortableDevice.h
ms.openlocfilehash: 1f44f32ab19c5ad10cc9c8dd5bdb8816ccc944f6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105785161"
---
# <a name="video-properties"></a>Propriedades do vídeo

Os dispositivos portáteis do Windows oferecem suporte às seguintes propriedades de vídeo.



| Propriedade                                         | VarType        | Descrição                                                                                                                                                                                                                                             |
|--------------------------------------------------|----------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **\_autor de vídeo WPD \_**                           | **LPWStr do VT \_** | O autor do arquivo de vídeo.                                                                                                                                                                                                                           |
| **taxa de bits de \_ vídeo WPD \_**                          | **\_UI4 VT**    | A taxa de bits do arquivo de vídeo.                                                                                                                                                                                                                         |
| **\_tamanho do \_ buffer de vídeo WPD \_**                     | **\_UI4 VT**    | Um valor que especifica o tamanho de buffer de vídeo necessário para processar esse arquivo.                                                                                                                                                                              |
| **\_créditos de vídeo WPD \_**                          | **LPWStr do VT \_** | Os créditos que listam a projeção e a equipe do vídeo.                                                                                                                                                                                                    |
| **\_ \_ código FOURCC de vídeo WPD \_**                     | **VT \_ DWORD**  | O código FourCC registrado que indica o codec que foi usado para o arquivo de vídeo. Para obter uma lista de formatos FourCC, consulte o artigo [registrou códigos FOURCC e formatos de onda](https://msdn2.microsoft.com/library/ms867195.aspx) no site do MSDN. |
| **taxa de quadros de \_ vídeo WPD \_**                        | **\_UI4 VT**    | A taxa de quadros do arquivo de vídeo, em quadros/segundo x 1.000. Por exemplo, uma taxa de quadros de 29,97 é representada como 29970.                                                                                                                                 |
| **\_gênero de vídeo WPD \_**                            | **LPWStr do VT \_** | O gênero deste arquivo de vídeo. Não há definições de gênero padrão.                                                                                                                                                                                  |
| **\_distância do \_ quadro da chave de vídeo WPD \_ \_**             | **\_UI4 VT**    | O intervalo entre os quadros-chave, em milissegundos.                                                                                                                                                                                                       |
| **\_configuração de \_ qualidade de vídeo WPD \_**                 | **\_UI4 VT**    | A configuração de qualidade do arquivo de vídeo. Isso depende do codec.                                                                                                                                                                                        |
| **\_número de \_ \_ canal RECORDEDTV de vídeo \_ WPD**      | **\_UI4 VT**    | O número do canal de televisão do qual o vídeo foi gravado.                                                                                                                                                                                              |
| **\_Descrição do \_ \_ programa RECORDEDTV de vídeo \_ WPD** | **LPWStr do VT \_** | Uma descrição do programa de televisão gravado.                                                                                                                                                                                                       |
| **\_repetição de \_ RECORDEDTV de vídeo WPD \_**               | **BOOL do VT \_**   | Um valor booliano que especifica se o programa de televisão foi uma repetição em exibição.                                                                                                                                                                     |
| **\_nome da \_ \_ estação RECORDEDTV de vídeo \_ WPD**        | **LPWStr do VT \_** | A estação de televisão da qual o vídeo foi gravado.                                                                                                                                                                                                |
| **\_tipo de \_ exame de vídeo WPD \_**                       | **\_UI4 VT**    | Um enumerador de [**\_ tipos de \_ verificação \_ de vídeo WPD**](wpd-video-scan-types.md) que especifica o entrelaçamento do arquivo de vídeo.                                                                                                                                  |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------|---------------------------------------------------------------------------------------------|
| parâmetro<br/> | <dl> <dt>PortableDevice. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Propriedades e atributos WPD**](properties-and-attributes.md)
</dt> </dl>

 

 




