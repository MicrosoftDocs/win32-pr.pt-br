---
description: Especifica o formato de destino para um codificador.
ms.assetid: 3d316561-352f-44f9-9978-01301a68e7b6
title: Propriedade AVEncCommonFormatConstraint (Codecapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 71e79536959aaaa0c50403bdd79d005bd48c729e
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "105755372"
---
# <a name="avenccommonformatconstraint-property"></a>Propriedade AVEncCommonFormatConstraint

Especifica o formato de destino para um codificador.

Esta propriedade é de leitura/gravação.

## <a name="data-type"></a>Tipo de dados

**BSTR** (**VT \_ BSTR**)

## <a name="property-guid"></a>GUID da propriedade

**CODECAPI \_ AVEncCommonFormatConstraint**

## <a name="property-value"></a>Valor da propriedade

O valor dessa propriedade é um **BSTR** que contém a representação de cadeia de caracteres de um GUID. Os GUIDs a seguir são definidos.



| GUID                                         | Descrição                     |
|----------------------------------------------|---------------------------------|
| CODECAPI \_ GUID \_ AVEncCommonFormatATSC        | Televisão do cabo ATSC.          |
| CODECAPI \_ GUID \_ AVEncCommonFormatDVB         | Televisão a cabo DVB.           |
| CODECAPI \_ GUID \_ AVEncCommonFormatDVD \_ DashVR | DVD-VR                          |
| CODECAPI \_ GUID \_ AVEncCommonFormatDVD \_ PlusVR | DVD + VR                          |
| CODECAPI \_ GUID \_ AVEncCommonFormatDVD \_ V      | DVD-Video                       |
| CODECAPI \_ GUID \_ AVEncCommonFormatHighMAT     | Fáceis                         |
| CODECAPI \_ GUID \_ AVEncCommonFormatHighMPV     | Não documentado nesta versão. |
| CODECAPI \_ GUID \_ AVEncCommonFormatMP3         | Camada de áudio MPEG-3 (MP3)        |
| CODECAPI \_ GUID \_ AVEncCommonFormatSVCD        | CD de supervídeo (SVCD)           |
| CODECAPI \_ GUID \_ AVEncCommonFormatUnSpecified | Formato não especificado.             |
| CODECAPI \_ GUID \_ AVEncCommonFormatVCD         | CD de vídeo (VCD)                  |



 

## <a name="remarks"></a>Comentários

Os aplicativos podem definir essa propriedade para especificar o formato de destino. Os codificadores também podem retornar essa propriedade como um recurso.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Aplicativos do Windows 2000 Professional \[ Desktop aplicativos \| UWP\]<br/>                     |
| Servidor mínimo com suporte<br/> | Aplicativos da área de trabalho do Windows 2000 Server aplicativos \[ \| UWP\]<br/>                           |
| parâmetro<br/>                   | <dl> <dt>Codecapi. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Propriedades da API do codec](codec-api-properties.md)
</dt> <dt>

[**Interface ICodecAPI**](/windows/desktop/api/Strmif/nn-strmif-icodecapi)
</dt> </dl>

 

 




