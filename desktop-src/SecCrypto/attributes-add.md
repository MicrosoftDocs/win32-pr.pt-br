---
description: Adiciona um objeto de atributo à coleção.
ms.assetid: dc2fe542-7168-4ffa-a10d-b2c051c4d42c
title: Método Attributes. Add
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Attributes.Add
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 824bff2fcca190e25f9b9c63ba0964674aff9fb7
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105770255"
---
# <a name="attributesadd-method"></a>Método Attributes. Add

\[O CAPICOM é um componente somente de 32 bits que está disponível para uso nos seguintes sistemas operacionais: Windows Server 2008, Windows Vista, Windows XP. Em vez disso, use a [**classe CryptographicAttributeObjectCollection**](/dotnet/api/system.security.cryptography.cryptographicattributeobjectcollection?view=dotnet-plat-ext-3.1&preserve-view=true) no namespace [**System. Security. Cryptography**](/previous-versions/windows/) .\]

O método **Add** adiciona um objeto de [**atributo**](attribute.md) à coleção.

## <a name="syntax"></a>Sintaxe


```VB
Attributes.Add( _
  ByVal Attribute _
)
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*Atributo* \[ no\]
</dt> <dd>

O objeto de [**atributo**](attribute.md) a ser adicionado ao final da coleção.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Esse método não retorna um valor. Um aplicativo que usa esse método deve conter código para manipular uma exceção gerada por esse método.

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

 

 
