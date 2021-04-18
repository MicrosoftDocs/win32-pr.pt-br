---
description: Exibe uma caixa de diálogo para selecionar certificados e retorna uma coleção desses certificados selecionados.
ms.assetid: dbf49a4b-6da1-4819-afcd-46db89a00fce
title: 'Método ICertificates2:: SELECT'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Certificates.Select
- ICertificates2.Select
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: cfd5b1cb5e269c14e05de25262fda711549bf02d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105760017"
---
# <a name="icertificates2select-method"></a>Método ICertificates2:: SELECT

\[O CAPICOM é um componente somente de 32 bits que está disponível para uso nos seguintes sistemas operacionais: Windows Server 2008, Windows Vista e Windows XP. Em vez disso, use a [**classe X509Certificate2Collection**](/previous-versions/windows/embedded/hh424013(v=msdn.10)) no namespace [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) .\]

O método **Select** exibe uma caixa de diálogo para selecionar certificados e retorna uma coleção desses certificados selecionados. Esse método foi introduzido no CAPICOM 2,0.

## <a name="syntax"></a>Sintaxe


```VB
Certificates.Select( _
  [ ByVal Title ], _
  [ ByVal DisplayString ], _
  [ ByVal bMultiSelect ] _
)
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*Título* \[ do em, opcional\]
</dt> <dd>

Cadeia de caracteres que contém o título da caixa de diálogo. O valor padrão é uma cadeia de caracteres vazia ("").

</dd> <dt>

*DisplayString* \[ em, opcional\]
</dt> <dd>

Cadeia de caracteres que contém o texto do prompt exibido com a caixa de diálogo. O valor padrão é uma cadeia de caracteres vazia ("").

</dd> <dt>

*bMultiSelect* \[ em, opcional\]
</dt> <dd>

Valor booliano que indica se o usuário pode selecionar mais de um certificado. Verdadeiro indica que vários certificados podem ser selecionados usando a tecla CTRL ou SHIFT. O valor padrão é false.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Um objeto de [**certificados**](certificates.md) que contém os certificados selecionados na caixa de diálogo.

**Capicom 2,1:** O objeto [**Certificates**](certificates.md) retornado contém referências aos certificados na coleção da qual a seleção foi feita. Todas as alterações feitas nos certificados no objeto de **certificados** retornados são refletidas nessa coleção.

**Capicom 2,0, CApicom 2.0.0.1, CApicom 2.0.0.2 e CApicom 2.0.0.3:** O objeto [**Certificates**](certificates.md) retornado contém cópias dos certificados na coleção da qual a seleção foi feita. As alterações feitas nos certificados no objeto de **certificados** retornados não são refletidas nessa coleção.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|----------------------------------|----------------------------------------------------------------------------------------|
| Fim do suporte do cliente<br/> | Windows Vista<br/>                                                               |
| Fim do suporte do servidor<br/> | Windows Server 2008<br/>                                                         |
| Redistribuível<br/>       | CAPICOM 2,0 ou posterior no Windows Server 2003 e no Windows XP<br/>                  |
| DLL<br/>                   | <dl> <dt>Capicom.dll</dt> </dl> |



 

 
