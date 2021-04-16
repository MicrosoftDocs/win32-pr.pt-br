---
description: Retorna uma representação de cadeia de caracteres dos dados codificados.
ms.assetid: d1231e6d-57d7-4b5a-ab37-d4ee1b29cf25
title: Método EncodedData. Format
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EncodedData.Format
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 435d0fdcd6e2bbd8c446c38f97012d820dbe5c7b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105750498"
---
# <a name="encodeddataformat-method"></a>Método EncodedData. Format

\[O CAPICOM é um componente somente de 32 bits que está disponível para uso nos seguintes sistemas operacionais: Windows Server 2008, Windows Vista e Windows XP. Em vez disso, use a [**classe AsnEncodedData**](/dotnet/api/system.security.cryptography.asnencodeddata?view=netcore-3.1) no namespace [**System. Security. Cryptography**](/dotnet/api/system.security.cryptography?view=dotnet-plat-ext-3.1&preserve-view=true) .\]

O método **Format** retorna uma representação de cadeia de caracteres dos dados codificados.

## <a name="syntax"></a>Sintaxe


```VB
EncodedData.Format( _
  [ ByVal bMultiLines ] _
)
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*bMultiLines* \[ em, opcional\]
</dt> <dd>

Valor booliano que indica se a cadeia de caracteres retornada contém várias linhas. Se **for true**, a cadeia de caracteres retornada poderá conter várias linhas separadas por **vbCrLf**. O valor padrão é **Falso**.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Uma cadeia de caracteres legível que representa os dados codificados. Se o CAPICOM não entender os dados codificados, uma representação hexadecimal dos dados será retornada.

## <a name="remarks"></a>Comentários

O formato da cadeia de caracteres retornada pode mudar entre versões diferentes do CAPICOM. Não confie em nenhum formato específico em seu aplicativo.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|----------------------------------|----------------------------------------------------------------------------------------|
| Fim do suporte do cliente<br/> | Windows Vista<br/>                                                               |
| Fim do suporte do servidor<br/> | Windows Server 2008<br/>                                                         |
| Redistribuível<br/>       | CAPICOM 2,0 ou posterior no Windows Server 2003 e no Windows XP<br/>                  |
| DLL<br/>                   | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**EncodedData**](encodeddata.md)
</dt> </dl>

 

 
