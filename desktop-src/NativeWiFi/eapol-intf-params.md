---
description: Contém parâmetros de configuração EAPOL.
ms.assetid: 4157a643-86f2-4f6f-8517-6207b11ea9a1
title: Estrutura de EAPOL_INTF_PARAMS (wzcsapi. h)
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
ms.openlocfilehash: dd9e0664fe41b471162beccd31bf2c22fbfa1640
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105780941"
---
# <a name="eapol_intf_params-structure"></a>Estrutura de parâmetros de EAPOL \_ INTF \_

\[**EAPOL \_ Não há mais suporte para \_ params INTF** a partir do Windows Vista e do windows Server 2008. Em vez disso, use a [API Wi-Fi nativa](native-wifi-reference.md), que fornece funcionalidade semelhante. Para obter mais informações, consulte [sobre a API Wi-Fi nativa](about-the-native-wifi-api.md).\]

Contém parâmetros de configuração EAPOL.

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

**DW**
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

**bSSID**
</dt> <dd>

Identificador de rede.

</dd> </dl>

## <a name="remarks"></a>Comentários

O arquivo de cabeçalho wzcsapi. h não está disponível no SDK do Windows.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos de área de trabalho do Windows XP com SP2\]<br/>                                 |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2003\]<br/>                                 |
| Fim do suporte do cliente<br/>    | Windows XP com SP3<br/>                                                       |
| Fim do suporte do servidor<br/>    | Windows Server 2003<br/>                                                       |
| parâmetro<br/>                   | <dl> <dt>Wzcsapi. h</dt> </dl> |



 

 




