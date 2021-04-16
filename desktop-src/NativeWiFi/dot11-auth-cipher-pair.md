---
description: Define um par de algoritmos de autenticação e codificação 802,11 que podem ser habilitados ao mesmo tempo na estação 802,11.
ms.assetid: 5fbe23f6-7902-46d4-a1f0-57f045d78662
title: Estrutura de DOT11_AUTH_CIPHER_PAIR (Wlantypes. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DOT11_AUTH_CIPHER_PAIR
api_type:
- HeaderDef
api_location:
- wlantypes.h
ms.openlocfilehash: fd1a8ef03d5c5cb897d95b768f8ab48705098d74
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105758183"
---
# <a name="dot11_auth_cipher_pair-structure"></a>\_Estrutura de \_ par de codificação de DOT11 auth \_

A estrutura de **\_ par de \_ codificação \_ de DOT11 auth** define um par de algoritmos de autenticação e codificação 802,11 que pode ser habilitado ao mesmo tempo na estação 802,11.

## <a name="syntax"></a>Sintaxe


```C++
typedef struct _DOT11_AUTH_CIPHER_PAIR {
  DOT11_AUTH_ALGORITHM   AuthAlgoId;
  DOT11_CIPHER_ALGORITHM CipherAlgoId;
} DOT11_AUTH_CIPHER_PAIR, *PDOT11_AUTH_CIPHER_PAIR;
```



## <a name="members"></a>Membros

<dl> <dt>

**AuthAlgoId**
</dt> <dd>

Um algoritmo de autenticação que usa um tipo enumerado de [**\_ \_ algoritmo DOT11 auth**](dot11-auth-algorithm.md) .

</dd> <dt>

**CipherAlgoId**
</dt> <dd>

Um algoritmo de codificação que usa um tipo enumerado de [**\_ \_ algoritmo DOT11 Cipher**](dot11-cipher-algorithm.md) .

</dd> </dl>

## <a name="remarks"></a>Comentários

A estrutura de par de codificação de DOT11 \_ auth \_ \_ define um algoritmo de autenticação e codificação que pode ser habilitado junto para conexões de rede de BSS (conjunto de serviços básico).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-------------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Somente Windows Vista, Windows XP com \[ aplicativos de área de trabalho do SP3\]<br/>                                         |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2008\]<br/>                                                        |
| Redistribuível<br/>          | API de LAN sem fio para Windows XP com SP2<br/>                                                         |
| parâmetro<br/>                   | <dl> <dt>Wlantypes. h (incluir Windot11. h)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**\_Algoritmo de autenticação DOT11 \_**](dot11-auth-algorithm.md)
</dt> <dt>

[**\_Algoritmo de codificação DOT11 \_**](dot11-cipher-algorithm.md)
</dt> </dl>

 

 




