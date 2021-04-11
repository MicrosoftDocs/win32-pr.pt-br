---
description: Cria um novo catálogo personalizado no indexador do Windows Search e retorna uma referência a ele.
ms.assetid: 2ADC48B8-87A2-4527-9AA8-9B0BA3A12462
title: 'Método ISearchManager2:: createcatalog'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISearchManager2.CreateCatalog
api_type:
- COM
api_location:
- searchapi.h
ms.openlocfilehash: 009e34a2d1eb4d18df1747ba01ea39c3360ec81a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104164327"
---
# <a name="isearchmanager2createcatalog-method"></a><span data-ttu-id="7de01-103">Método ISearchManager2:: createcatalog</span><span class="sxs-lookup"><span data-stu-id="7de01-103">ISearchManager2::CreateCatalog method</span></span>

<span data-ttu-id="7de01-104">Cria um novo catálogo personalizado no indexador do Windows Search e retorna uma referência a ele.</span><span class="sxs-lookup"><span data-stu-id="7de01-104">Creates a new custom catalog in the Windows Search indexer and returns a reference to it.</span></span>

## <a name="syntax"></a><span data-ttu-id="7de01-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="7de01-105">Syntax</span></span>


```C++
HRESULT CreateCatalog(
  [in]  LPCWSTR               pszCatalog,
  [out] ISearchCatalogManager **ppCatalogManager
);
```



## <a name="parameters"></a><span data-ttu-id="7de01-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="7de01-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7de01-107">*pszCatalog* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="7de01-107">*pszCatalog* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7de01-108">Tipo: **[ **LPCWSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="7de01-108">Type: **[**LPCWSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="7de01-109">Nome do catálogo a ser criado.</span><span class="sxs-lookup"><span data-stu-id="7de01-109">Name of catalog to create.</span></span> <span data-ttu-id="7de01-110">Pode ser qualquer nome selecionado pelo chamador, deve conter apenas caracteres alfanuméricos padrão e sublinhado.</span><span class="sxs-lookup"><span data-stu-id="7de01-110">Can be any name selected by the caller, must contain only standard alphanumeric characters and underscore.</span></span>

</dd> <dt>

<span data-ttu-id="7de01-111">*ppCatalogManager* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="7de01-111">*ppCatalogManager* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="7de01-112">Tipo: **[ **ISearchCatalogManager**](/windows/desktop/api/Searchapi/nn-searchapi-isearchcatalogmanager)\*\***</span><span class="sxs-lookup"><span data-stu-id="7de01-112">Type: **[**ISearchCatalogManager**](/windows/desktop/api/Searchapi/nn-searchapi-isearchcatalogmanager)\*\***</span></span>

<span data-ttu-id="7de01-113">Em caso de sucesso, uma referência ao catálogo criado é retornada como um ponteiro de interface [**ISearchCatalogManager**](/windows/desktop/api/Searchapi/nn-searchapi-isearchcatalogmanager) .</span><span class="sxs-lookup"><span data-stu-id="7de01-113">On success a reference to the created catalog is returned as an [**ISearchCatalogManager**](/windows/desktop/api/Searchapi/nn-searchapi-isearchcatalogmanager) interface pointer.</span></span> <span data-ttu-id="7de01-114">A versão () deve ser chamada nesta interface depois que o aplicativo de chamada terminar de usá-la.</span><span class="sxs-lookup"><span data-stu-id="7de01-114">The Release() must be called on this interface after the calling application has finished using it.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7de01-115">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="7de01-115">Return value</span></span>

<span data-ttu-id="7de01-116">Tipo: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="7de01-116">Type: **HRESULT**</span></span>

<span data-ttu-id="7de01-117">HRESULT indicando o status da operação:</span><span class="sxs-lookup"><span data-stu-id="7de01-117">HRESULT indicating status of operation:</span></span>



| <span data-ttu-id="7de01-118">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="7de01-118">Return code</span></span>                                                                             | <span data-ttu-id="7de01-119">Descrição</span><span class="sxs-lookup"><span data-stu-id="7de01-119">Description</span></span>                                                                                 |
|-----------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="7de01-120"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="7de01-120"><dt>**S\_OK**</dt></span></span> </dl>    | <span data-ttu-id="7de01-121">O catálogo não existia e foi criado anteriormente.</span><span class="sxs-lookup"><span data-stu-id="7de01-121">Catalog did not previously exist and was created.</span></span> <span data-ttu-id="7de01-122">Referência ao catálogo retornada.</span><span class="sxs-lookup"><span data-stu-id="7de01-122">Reference to catalog returned.</span></span><br/> |
| <dl> <span data-ttu-id="7de01-123"><dt>**\_falso**</dt></span><span class="sxs-lookup"><span data-stu-id="7de01-123"><dt>**S\_FALSE**</dt></span></span> </dl> | <span data-ttu-id="7de01-124">O catálogo já existia, referência ao catálogo retornada.</span><span class="sxs-lookup"><span data-stu-id="7de01-124">Catalog previously existed, reference to catalog returned.</span></span><br/>                       |



 

<span data-ttu-id="7de01-125">HRESULT com falha: falha ao criar catálogo ou argumentos inválidos passados.</span><span class="sxs-lookup"><span data-stu-id="7de01-125">FAILED HRESULT: Failure creating catalog or invalid arguments passed.</span></span>

## <a name="remarks"></a><span data-ttu-id="7de01-126">Comentários</span><span class="sxs-lookup"><span data-stu-id="7de01-126">Remarks</span></span>

<span data-ttu-id="7de01-127">Chamado para criar um novo catálogo no indexador do Windows Search.</span><span class="sxs-lookup"><span data-stu-id="7de01-127">Called to create a new catalog in the Windows Search indexer.</span></span> <span data-ttu-id="7de01-128">Após a criação, os métodos no Gerenciador de [**ISearchCatalog**](/windows/desktop/api/Searchapi/nn-searchapi-isearchcatalogmanager) retornado podem ser usados para adicionar locais a serem indexados, monitorar o processo de indexação e construir consultas para enviar ao indexador e obter resultados.</span><span class="sxs-lookup"><span data-stu-id="7de01-128">After creation, the methods on the returned [**ISearchCatalog**](/windows/desktop/api/Searchapi/nn-searchapi-isearchcatalogmanager) manager can be used to add locations to be indexed, monitor indexing process, and construct queries to send to the indexer and get results.</span></span> <span data-ttu-id="7de01-129">Consulte a documentação "Gerenciando o índice" para obter mais informações: https://msdn.microsoft.com/library/bb266516(VS.85).aspx</span><span class="sxs-lookup"><span data-stu-id="7de01-129">See the “Managing the Index” documentation for more info: https://msdn.microsoft.com/library/bb266516(VS.85).aspx</span></span>

## <a name="requirements"></a><span data-ttu-id="7de01-130">Requisitos</span><span class="sxs-lookup"><span data-stu-id="7de01-130">Requirements</span></span>



| <span data-ttu-id="7de01-131">Requisito</span><span class="sxs-lookup"><span data-stu-id="7de01-131">Requirement</span></span> | <span data-ttu-id="7de01-132">Valor</span><span class="sxs-lookup"><span data-stu-id="7de01-132">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="7de01-133">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="7de01-133">Minimum supported client</span></span><br/> | <span data-ttu-id="7de01-134">\[Somente aplicativos de área de trabalho do Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="7de01-134">Windows 8 \[desktop apps only\]</span></span><br/>           |
| <span data-ttu-id="7de01-135">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="7de01-135">Minimum supported server</span></span><br/> | <span data-ttu-id="7de01-136">\[Somente aplicativos da área de trabalho do Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="7de01-136">Windows Server 2012 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="7de01-137">Confira também</span><span class="sxs-lookup"><span data-stu-id="7de01-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7de01-138">**ISearchManager2**</span><span class="sxs-lookup"><span data-stu-id="7de01-138">**ISearchManager2**</span></span>](/windows/desktop/api/searchapi/nn-searchapi-isearchmanager2)
</dt> </dl>

 

 
