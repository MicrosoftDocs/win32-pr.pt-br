---
description: Armazena as principais informações sobre uma interface de LAN sem fio gerenciada pelo serviço de configuração sem fio.
ms.assetid: 5e689fd0-27d9-48eb-8983-96d7918be1cd
title: Estrutura de INTF_KEY_ENTRY (wzcsapi. h)
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
ms.openlocfilehash: 91f25708e79be4f85c4200bd690404ff39f567d5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104296428"
---
# <a name="intf_key_entry-structure"></a>Estrutura de entrada de \_ chave INTF \_

\[**INTF \_ A \_ entrada de chave** não tem mais suporte do Windows Vista e do windows Server 2008. Em vez disso, use a [API Wi-Fi nativa](native-wifi-reference.md), que fornece funcionalidade semelhante. Para obter mais informações, consulte [sobre a API Wi-Fi nativa](about-the-native-wifi-api.md).\]

A estrutura de **\_ \_ entrada de chave INTF** armazena as principais informações sobre uma interface de LAN sem fio gerenciada pelo serviço de configuração sem fio.

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
> O arquivo de cabeçalho *wzcsapi. h* não está disponível no SDK do Windows.

 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos de área de trabalho do Windows XP com SP2\]<br/>                                 |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2003\]<br/>                                 |
| Fim do suporte do cliente<br/>    | Windows XP com SP3<br/>                                                       |
| Fim do suporte do servidor<br/>    | Windows Server 2003<br/>                                                       |
| parâmetro<br/>                   | <dl> <dt>Wzcsapi. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**\_tabela de chave INTFS \_**](intfs-key-table.md)
</dt> <dt>

[**WZCEnumInterfaces**](wzcenuminterfaces.md)
</dt> </dl>

 

 




