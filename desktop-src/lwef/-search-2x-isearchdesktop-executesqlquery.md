---
title: Método ISearchDesktop ExecuteSQLQuery
description: Usa um ponteiro para uma cadeia de caracteres que contém uma consulta linguagem SQL (SQL) e seus atributos e retorna um ponteiro para o conjunto de retorno.
ms.assetid: df3f473b-0bee-4035-abf8-dbe5249ef0ed
keywords:
- Recursos do ambiente Windows herdado do método ExecuteSQLQuery
- Método ExecuteSQLQuery de recursos de ambiente do Windows herdados, interface ISearchDesktop
- Recursos do ambiente Windows herdado da interface ISearchDesktop, método ExecuteSQLQuery
topic_type:
- apiref
api_name:
- ISearchDesktop.ExecuteSQLQuery
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: f0b13ff361d07f99efe1366e2201d610eac10523
ms.sourcegitcommit: b9a94cea8f83153214af4c09509e1cc61a1bb616
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/19/2020
ms.locfileid: "103640276"
---
# <a name="isearchdesktopexecutesqlquery-method"></a>Método ISearchDesktop:: ExecuteSQLQuery

> [!NOTE]
> O Windows Desktop Search 2. x é uma tecnologia obsoleta que originalmente estava disponível como um suplemento para o Windows XP e o Windows Server 2003. Em versões posteriores, use a [API de pesquisa do Windows](../search/-search-reference-entry-page.md) em vez disso. 

Usa um ponteiro para uma cadeia de caracteres que contém uma consulta linguagem SQL (SQL) e seus atributos e retorna um ponteiro para o conjunto de retorno.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT ExecuteSQLQuery(
  [in]  LPCWSTR *pdwAttributes,
  [in]  LPCWSTR pwszURL,
  [out] ppidUrl *ppidUrl
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pdwAttributes* \[ no\]
</dt> <dd>

Tipo: **LPCWSTR \***

Uma cadeia de caracteres que contém os outros atributos para a consulta.

</dd> <dt>

*pwszURL* \[ no\]
</dt> <dd>

Tipo: **LPCWSTR**

Uma cadeia de caracteres que contém a consulta SQL.

</dd> <dt>

*ppidUrl* \[ fora\]
</dt> <dd>

Tipo: **ppidUrl \***

Quando esse método retorna com êxito, contém um ponteiro para o conjunto de registros retornado.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Tipo: **HRESULT**

Se esse método for bem sucedido, ele retornará **S \_ OK**. Caso contrário, ele retorna um código de erro **HRESULT** .

 

 




