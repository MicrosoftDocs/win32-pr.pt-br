---
description: Armazena as principais informações sobre uma interface de LAN sem fio gerenciada pelo Serviço de Configuração Sem Fio.
ms.assetid: 5e689fd0-27d9-48eb-8983-96d7918be1cd
title: INTF_KEY_ENTRY (Wzcsapi.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- INTF_KEY_ENTRY
api_type:
- HeaderDef
api_location:
- wzcsapi.h
ms.openlocfilehash: 8d14c65d49d7ed28e2756c2a690cb4a7efa9000417e896a206710bf4365f8cd4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119065146"
---
# <a name="intf_key_entry-structure"></a>Estrutura INTF \_ KEY \_ ENTRY

\[**INTF \_ Não \_ há** mais suporte para KEY ENTRY a partir do Windows Vista e Windows Server 2008. Em vez disso, use [a API Wi-Fi](native-wifi-reference.md)Nativa , que fornece funcionalidade semelhante. Para obter mais informações, consulte [Sobre a API Wifi nativa.](about-the-native-wifi-api.md)\]

A **estrutura INTF \_ KEY \_ ENTRY** armazena as principais informações sobre uma interface de LAN sem fio gerenciada pelo Serviço de Configuração Sem Fio.

## <a name="syntax"></a>Sintaxe


```C++
typedef struct {
  LPWSTR wszGuid;
} INTF_KEY_ENTRY, *PINTF_KEY_ENTRY;
```



## <a name="members"></a>Membros

<dl> <dt>

**wszGuid**
</dt> <dd>

Um ponteiro para o GUID da interface representado como uma cadeia de caracteres Unicode no seguinte formato: "{xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx}".

</dd> </dl>

## <a name="remarks"></a>Comentários

> [!Note]  
> O *arquivo de título Wzcsapi.h* não está disponível no SDK do Windows.

 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows XP somente com \[ aplicativos da área de trabalho SP2\]<br/>                                 |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho server 2003 \[\]<br/>                                 |
| Fim do suporte ao cliente<br/>    | Windows XP com SP3<br/>                                                       |
| Fim do suporte ao servidor<br/>    | Windows Server 2003<br/>                                                       |
| Cabeçalho<br/>                   | <dl> <dt>Wzcsapi.h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**INTFS \_ KEY \_ TABLE**](intfs-key-table.md)
</dt> <dt>

[**WZCEnumInterfaces**](wzcenuminterfaces.md)
</dt> </dl>

 

 




