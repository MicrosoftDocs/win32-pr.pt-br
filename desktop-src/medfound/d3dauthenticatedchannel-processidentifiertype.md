---
description: Especifica o tipo de processo que é identificado na estrutura de \_ saída D3DAUTHENTICATEDCHANNEL QUERYRESTRICTEDSHAREDRESOURCEPROCESS \_ .
ms.assetid: 8878905e-f55b-4dbc-9608-da0082daf673
title: Enumeração de D3DAUTHENTICATEDCHANNEL_PROCESSIDENTIFIERTYPE (D3d9types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DAUTHENTICATEDCHANNEL_PROCESSIDENTIFIERTYPE
api_type:
- HeaderDef
api_location:
- d3d9types.h
ms.openlocfilehash: 1b2fdb7384ff868b02f54650de9662b297ce39db
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104089765"
---
# <a name="d3dauthenticatedchannel_processidentifiertype-enumeration"></a>\_Enumeração D3DAUTHENTICATEDCHANNEL PROCESSIDENTIFIERTYPE

Especifica o tipo de processo que é identificado na estrutura [**de \_ \_ saída D3DAUTHENTICATEDCHANNEL QUERYRESTRICTEDSHAREDRESOURCEPROCESS**](d3dauthenticatedchannel-queryrestrictedsharedresourceprocess-output.md) .

## <a name="syntax"></a>Sintaxe


```C++
typedef enum  { 
  PROCESSIDTYPE_UNKNOWN  = 0,
  PROCESSIDTYPE_DWM      = 1,
  PROCESSIDTYPE_HANDLE   = 2
} D3DAUTHENTICATEDCHANNEL_PROCESSIDENTIFIERTYPE;
```



## <a name="constants"></a>Constantes

<dl> <dt>

<span id="PROCESSIDTYPE_UNKNOWN"></span><span id="processidtype_unknown"></span>**PROCESSIDtype \_ desconhecido**
</dt> <dd>

Tipo de processo desconhecido.

</dd> <dt>

<span id="PROCESSIDTYPE_DWM"></span><span id="processidtype_dwm"></span>**DWM do PROCESSIDtype \_**
</dt> <dd>

Processo de Gerenciador de Janelas da Área de Trabalho (DWM).

</dd> <dt>

<span id="PROCESSIDTYPE_HANDLE"></span><span id="processidtype_handle"></span>**identificador de PROCESSIDtype \_**
</dt> <dd>

Identificador para um processo.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos de área de trabalho do Windows 7\]<br/>                                                              |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2008 R2\]<br/>                                                 |
| parâmetro<br/>                   | <dl> <dt>D3d9types. h (incluir D3d9. h)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Enumerações de vídeo do Direct3D](direct3d-video-enumerations.md)
</dt> </dl>

 

 




