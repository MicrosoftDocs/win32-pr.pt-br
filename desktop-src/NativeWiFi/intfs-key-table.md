---
description: Contém a tabela de informações de chave para todas as interfaces de LAN sem fio gerenciadas pelo serviço de configuração sem fio.
ms.assetid: 5d5fe222-6ca1-4778-9f64-1c6a63467a6c
title: Estrutura de INTFS_KEY_TABLE (wzcsapi. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- INTFS_KEY_TABLE
api_type:
- HeaderDef
api_location:
- Wzcsapi.h
ms.openlocfilehash: 5e1aee9708721036fba487edafa901ec701156d44d3f6cb76265d49701925cef
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117984976"
---
# <a name="intfs_key_table-structure"></a>Estrutura de tabela de \_ chave INTFS \_

\[**INTFS \_ a \_ tabela de chave** não tem mais suporte a partir do Windows Vista e do Windows Server 2008. Em vez disso, use a [API Wi-Fi nativa](native-wifi-reference.md), que fornece funcionalidade semelhante. Para obter mais informações, consulte [sobre a API Wi-Fi nativa](about-the-native-wifi-api.md).\]

A estrutura da **\_ \_ tabela de chave INTFS** contém a tabela de informações de chave para todas as interfaces de LAN sem fio gerenciadas pelo serviço de configuração sem fio.

## <a name="syntax"></a>Sintaxe


```C++
typedef struct {
  DWORD           dwNumIntfs;
  PINTF_KEY_ENTRY pIntfs;
} INTFS_KEY_TABLE, *PINTFS_KEY_TABLE;
```



## <a name="members"></a>Membros

<dl> <dt>

**dwNumIntfs**
</dt> <dd>

Número total de interfaces.

</dd> <dt>

**pIntfs**
</dt> <dd>

Ponteiro para a estrutura de [**\_ \_ entrada de chave INTF**](intf-key-entry.md) .

</dd> </dl>

## <a name="remarks"></a>Comentários

> [!Note]  
> o arquivo de cabeçalho *Wzcsapi. h* não está disponível no SDK do Windows.

 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows XP somente com \[ aplicativos de área de trabalho do SP2\]<br/>                                 |
| Servidor mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do servidor 2003\]<br/>                                 |
| Fim do suporte do cliente<br/>    | Windows XP com SP3<br/>                                                       |
| Fim do suporte do servidor<br/>    | Windows Server 2003<br/>                                                       |
| Cabeçalho<br/>                   | <dl> <dt>Wzcsapi. h</dt> </dl> |



 

 




