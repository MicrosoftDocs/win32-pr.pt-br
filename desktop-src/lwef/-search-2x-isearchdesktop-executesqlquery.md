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
# <a name="isearchdesktopexecutesqlquery-method"></a><span data-ttu-id="4f70c-106">Método ISearchDesktop:: ExecuteSQLQuery</span><span class="sxs-lookup"><span data-stu-id="4f70c-106">ISearchDesktop::ExecuteSQLQuery method</span></span>

> [!NOTE]
> <span data-ttu-id="4f70c-107">O Windows Desktop Search 2. x é uma tecnologia obsoleta que originalmente estava disponível como um suplemento para o Windows XP e o Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="4f70c-107">Windows Desktop Search 2.x is an obsolete technology that was originally available as an add-in for Windows XP and Windows Server 2003.</span></span> <span data-ttu-id="4f70c-108">Em versões posteriores, use a [API de pesquisa do Windows](../search/-search-reference-entry-page.md) em vez disso.</span><span class="sxs-lookup"><span data-stu-id="4f70c-108">On later releases, use the [Windows Search API](../search/-search-reference-entry-page.md) instead.</span></span> 

<span data-ttu-id="4f70c-109">Usa um ponteiro para uma cadeia de caracteres que contém uma consulta linguagem SQL (SQL) e seus atributos e retorna um ponteiro para o conjunto de retorno.</span><span class="sxs-lookup"><span data-stu-id="4f70c-109">Takes a pointer to a string that contains a Structured Query Language (SQL) query and its attributes and returns a pointer to the return set.</span></span>

## <a name="syntax"></a><span data-ttu-id="4f70c-110">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="4f70c-110">Syntax</span></span>


```C++
HRESULT ExecuteSQLQuery(
  [in]  LPCWSTR *pdwAttributes,
  [in]  LPCWSTR pwszURL,
  [out] ppidUrl *ppidUrl
);
```



## <a name="parameters"></a><span data-ttu-id="4f70c-111">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="4f70c-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4f70c-112">*pdwAttributes* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="4f70c-112">*pdwAttributes* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4f70c-113">Tipo: **LPCWSTR \***</span><span class="sxs-lookup"><span data-stu-id="4f70c-113">Type: **LPCWSTR\***</span></span>

<span data-ttu-id="4f70c-114">Uma cadeia de caracteres que contém os outros atributos para a consulta.</span><span class="sxs-lookup"><span data-stu-id="4f70c-114">A string that contains the other attributes for the query.</span></span>

</dd> <dt>

<span data-ttu-id="4f70c-115">*pwszURL* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="4f70c-115">*pwszURL* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4f70c-116">Tipo: **LPCWSTR**</span><span class="sxs-lookup"><span data-stu-id="4f70c-116">Type: **LPCWSTR**</span></span>

<span data-ttu-id="4f70c-117">Uma cadeia de caracteres que contém a consulta SQL.</span><span class="sxs-lookup"><span data-stu-id="4f70c-117">A string that contains the SQL query.</span></span>

</dd> <dt>

<span data-ttu-id="4f70c-118">*ppidUrl* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="4f70c-118">*ppidUrl* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="4f70c-119">Tipo: **ppidUrl \***</span><span class="sxs-lookup"><span data-stu-id="4f70c-119">Type: **ppidUrl\***</span></span>

<span data-ttu-id="4f70c-120">Quando esse método retorna com êxito, contém um ponteiro para o conjunto de registros retornado.</span><span class="sxs-lookup"><span data-stu-id="4f70c-120">When this method returns successfully, contains a pointer to the returned recordset.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4f70c-121">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="4f70c-121">Return value</span></span>

<span data-ttu-id="4f70c-122">Tipo: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="4f70c-122">Type: **HRESULT**</span></span>

<span data-ttu-id="4f70c-123">Se esse método for bem sucedido, ele retornará **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="4f70c-123">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="4f70c-124">Caso contrário, ele retorna um código de erro **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="4f70c-124">Otherwise, it returns an **HRESULT** error code.</span></span>

 

 




