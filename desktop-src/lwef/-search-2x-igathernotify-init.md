---
title: Método IGatherNotify init (preterido)
description: este tópico Windows interface de pesquisa da área de trabalho foi preterido e é substituído pela API do ISearchPersistentItemsChangedSink search Windows no SDK do Windows. | Método IGatherNotify init (preterido)
ms.assetid: 6a5f89eb-10f4-4262-89bf-b47e345f12eb
keywords:
- método Init (preterido) Windows recursos de ambiente herdados
- método Init (preterido) herdado Windows recursos de ambiente, interface IGatherNotify
- IGatherNotify interface herdada Windows recursos do ambiente, método Init (preterido)
topic_type:
- apiref
api_name:
- IGatherNotify.Init (Deprecated)
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: db5666197524afb454927036cdd68375dfb2937197ed211646b63d80a09e5b12
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119359296"
---
# <a name="igathernotifyinit-deprecated-method"></a>Método IGatherNotify:: init (preterido)

\[**Init** pode ser alterado ou indisponível nas versões subsequentes do sistema operacional ou produto.\]

este tópico Windows interface de pesquisa da área de trabalho foi preterido e é substituído pela API do [**ISearchPersistentItemsChangedSink**](/windows/desktop/api/searchapi/nn-searchapi-isearchpersistentitemschangedsink) search Windows no SDK do Windows.

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

## <a name="return-value"></a>Valor retornado

Esse método não retorna um valor.

## <a name="remarks"></a>Comentários

inicialize com application = "RSApp", Project = "myindex".

 

 
