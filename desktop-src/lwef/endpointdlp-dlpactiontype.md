---
description: Especifica o tipo de ação de uma operação de DLP (prevenção de perda de dados) de ponto de extremidade.
title: Enumeração DlpActionType (endpointdlp. h)
ms.topic: reference
ms.date: 03/18/2021
topic_type:
- APIRef
- kbSyntax
api_name:
- DlpActionType
api_type:
- COM
api_location:
- endpointdlp.h
ms.openlocfilehash: 7900e79536cc9ac45037e205962a563bcde8878a
ms.sourcegitcommit: 91110c16e4713ed82d7fb80562d3ddf40b5d76b2
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/14/2021
ms.locfileid: "107495362"
---
# <a name="dlpactiontype-enumeration"></a>Enumeração DlpActionType

Especifica o tipo de ação de uma operação de DLP (prevenção de perda de dados) de ponto de extremidade.

## <a name="syntax"></a>Sintaxe


```C++
typedef enum  
{
    DlpActionTypeCopyToRemovableMedia = 0,
    DlpActionTypeCopyToNetworkShare = 1,
    DlpActionTypeCopyToClipboard = 2,
    DlpActionTypePrint = 3,
    DlpActionTypeScreenClip = 4,
    DlpActionTypeAccessByUnallowedApp = 5,
    DlpActionTypeCloudAppEgress = 6,
    DlpActionTypeAccessByBluetoothApp = 7,
    DlpActionTypeAccessByRDPApp = 8,
    DlpActionTypeCount = 9
} DlpActionType;
```


## <a name="constants"></a>Constantes

<dl> <dt>

*DlpActionTypeCopyToRemovableMedia*
</dt> <dd>

Uma operação de cópia para mídia removível.

</dd> </dl>

<dl> <dt>

*DlpActionTypeCopyToNetworkShare*
</dt> <dd>

Uma operação de cópia para uma pasta de rede compartilhada.

</dd> </dl>

<dl> <dt>

*DlpActionTypeCopyToClipboard*
</dt> <dd>

Uma operação de cópia para a área de transferência.

</dd> </dl>

<dl> <dt>

*DlpActionTypePrint*
</dt> <dd>

Uma operação de impressão.

</dd> </dl>


<dl> <dt>

*DlpActionTypeScreenClip*
</dt> <dd>

Uma operação de captura de tela.

</dd> </dl>

<dl> <dt>

*DlpActionTypeAccessByUnallowedApp*
</dt> <dd>

Uma operação executada por um aplicativo não permitido.

</dd> </dl>


<dl> <dt>

*DlpActionTypeCloudAppEgress*
</dt> <dd>

Uma operação direcionada a um local de nuvem.

</dd> </dl>

<dl> <dt>

*DlpActionTypeAccessByBluetoothApp*
</dt> <dd>

Uma operação que inclui o acesso por um aplicativo Bluetooth.

</dd> </dl>

<dl> <dt>

*DlpActionTypeAccessByRDPApp*
</dt> <dd>

Uma operação que inclui o acesso por uma área de trabalho remota.

</dd> </dl>

<dl> <dt>

*DlpActionTypeCount*
</dt> <dd>

O valor máximo da enumeração.

</dd> </dl>
 

## <a name="remarks"></a>Comentários

Os valores dessa enumeração são usados pela estrutura de [DLP_APP_OP_ENLIGHTENED_LEVEL](endpointdlp-dlp_app_op_enlightened_level.md) .

## <a name="requirements"></a>Requisitos



| Requisito          |    Valor                   |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 10, versão 1809 (10,0; Build 17763)           |

