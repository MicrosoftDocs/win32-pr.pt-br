---
title: Método IGatherNotify init (preterido)
description: Este tópico da interface do Windows Desktop Search foi preterido e é substituído pela API ISearchPersistentItemsChangedSink do Windows Search no SDK do Windows. | Método IGatherNotify init (preterido)
ms.assetid: 6a5f89eb-10f4-4262-89bf-b47e345f12eb
keywords:
- Método init (preterido) recursos de ambiente herdado do Windows
- Método init (preterido) recursos de ambiente herdado do Windows, interface IGatherNotify
- Recursos do ambiente Windows herdado da interface IGatherNotify, método init (preterido)
topic_type:
- apiref
api_name:
- IGatherNotify.Init (Deprecated)
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 81379bb4a9a7c6099912bfc9ebca170141d76cd2
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/09/2021
ms.locfileid: "105781439"
---
# <a name="igathernotifyinit-deprecated-method"></a>Método IGatherNotify:: init (preterido)

\[**Init** pode ser alterado ou indisponível nas versões subsequentes do sistema operacional ou produto.\]

Este tópico da interface do Windows Desktop Search foi preterido e é substituído pela API [**ISearchPersistentItemsChangedSink**](/windows/desktop/api/searchapi/nn-searchapi-isearchpersistentitemschangedsink) do Windows Search no SDK do Windows.

Inicializa a interface do gatherer. Também especifica o índice a ser notificado e a loja de aplicativos a ser monitorada.

## <a name="syntax"></a>Sintaxe


```C++
void Init (Deprecated)(
  [in] BSTR    bstrApplication,
  [in] BSTR    bstrProject,
  [in] variant varScopesBstrArray
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*bstrApplication* \[ no\]
</dt> <dd>

Tipo: **BSTR**

Uma cadeia de caracteres que especifica o aplicativo de destino.

</dd> <dt>

*bstrProject* \[ no\]
</dt> <dd>

Tipo: **BSTR**

Uma cadeia de caracteres que especifica o nome do indexador para o qual passar informações do gatherer.

</dd> <dt>

*varScopesBstrArray* \[ no\]
</dt> <dd>

Tipo: **variante**

Parâmetro opcional, que permite que você passe uma matriz de escopos a ser inicializada.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Esse método não retorna um valor.

## <a name="remarks"></a>Comentários

Inicialize com Application = "RSApp", Project = "MyIndex".

 

 
