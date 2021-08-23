---
description: Contém parâmetros de configuração de EAPOL.
ms.assetid: 4157a643-86f2-4f6f-8517-6207b11ea9a1
title: EAPOL_INTF_PARAMS (Wzcsapi.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EAPOL_INTF_PARAMS
api_type:
- HeaderDef
api_location:
- wzcsapi.h
ms.openlocfilehash: 3359454196735b8100ea40a9b4add2e8e0398c336bf254eb507b0a4e63a86e1e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119685235"
---
# <a name="eapol_intf_params-structure"></a>Estrutura \_ PARAMS INTF do EAPOL \_

\[**EAPOL \_ O \_ INTF PARAMS** não tem mais suporte a partir do Windows Vista e Windows Server 2008. Em vez disso, use [a API Wi-Fi](native-wifi-reference.md)Nativa , que fornece funcionalidade semelhante. Para obter mais informações, consulte [Sobre a API Wifi nativa.](about-the-native-wifi-api.md)\]

Contém parâmetros de configuração de EAPOL.

## <a name="syntax"></a>Sintaxe


```C++
typedef struct _EAPOL_INTF_PARAMS {
  DWORD dwVersion;
  DWORD dwReserved2;
  DWORD dwEapFlags;
  DWORD dwEapType;
  DWORD dwSizeOfSSID;
  BYTE  bSSID[MAX_NETWORK_NAME_LENGTH];
} EAPOL_INTF_PARAMS, *PEAPOL_INTF_PARAMS;
```



## <a name="members"></a>Membros

<dl> <dt>

**Dwversion**
</dt> <dd>

Versão do chamador. O padrão é 0.

</dd> <dt>

**dwReserved2**
</dt> <dd>

Reservado para uso futuro.

</dd> <dt>

**dwEapFlags**
</dt> <dd>

Não usado.

</dd> <dt>

**dwEapType**
</dt> <dd>

O tipo de extensão EAP a ser usado. Defina como 0x00000013 para EAP-TLS e 0x00000026 para PEAP.

</dd> <dt>

**dwSizeOfSSID**
</dt> <dd>

Tamanho do identificador de rede.

</dd> <dt>

**Bssid**
</dt> <dd>

Identificador de rede.

</dd> </dl>

## <a name="remarks"></a>Comentários

O arquivo de título wzcsapi.h não está disponível no SDK do Windows.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows XP somente com \[ aplicativos da área de trabalho SP2\]<br/>                                 |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho server 2003 \[\]<br/>                                 |
| Fim do suporte ao cliente<br/>    | Windows XP com SP3<br/>                                                       |
| Fim do suporte ao servidor<br/>    | Windows Server 2003<br/>                                                       |
| Cabeçalho<br/>                   | <dl> <dt>Wzcsapi.h</dt> </dl> |



 

 




