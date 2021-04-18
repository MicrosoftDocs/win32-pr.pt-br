---
description: Remove um objeto de atributo indexado da coleção.
ms.assetid: 6d9423e3-ab24-4973-b0aa-32e38abd607a
title: Método Attributes. Remove
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Attributes.Remove
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: e5981176afb332254d98171d40027e43383cb557
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105758924"
---
# <a name="attributesremove-method"></a>Método Attributes. Remove

\[O CAPICOM é um componente somente de 32 bits que está disponível para uso nos seguintes sistemas operacionais: Windows Server 2008, Windows Vista, Windows XP. Em vez disso, use a [**classe CryptographicAttributeObjectCollection**](/dotnet/api/system.security.cryptography.cryptographicattributeobjectcollection?view=dotnet-plat-ext-3.1&preserve-view=true) no namespace [**System. Security. Cryptography**](/dotnet/api/system.security.cryptography?view=dotnet-plat-ext-3.1&preserve-view=true) .\]

O método **Remove** remove um objeto de [**atributo**](attribute.md) indexado da coleção.

## <a name="syntax"></a>Sintaxe


```VB
Attributes.Remove( _
  ByVal Index _
)
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*Índice* \[ do no\]
</dt> <dd>

Índice do objeto de [**atributo**](attribute.md) a ser removido.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Esse método não retorna um valor.

## <a name="remarks"></a>Comentários

Os aplicativos que usam esse método devem conter código para manipular uma exceção gerada por esse método.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|----------------------------------|----------------------------------------------------------------------------------------|
| Fim do suporte do cliente<br/> | Windows Vista<br/>                                                               |
| Fim do suporte do servidor<br/> | Windows Server 2008<br/>                                                         |
| Redistribuível<br/>       | CAPICOM 2,0 ou posterior no Windows Server 2003 e no Windows XP<br/>                  |
| DLL<br/>                   | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Objetos de criptografia](cryptography-objects.md)
</dt> <dt>

[**Atributos**](attributes.md)
</dt> </dl>

 

 
