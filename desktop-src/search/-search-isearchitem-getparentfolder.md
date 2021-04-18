---
description: Obtém o objeto ISearchItem se a URL representa uma fonte de dados do Shell real (também conhecida como extensão de namespace do Shell).
ms.assetid: 7da6344d-b433-48c3-8f75-7bef0295b9ea
title: 'Método ISearchItem:: GetParentFolder'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISearchItem.GetParentFolder
api_type:
- COM
api_location: ''
ms.openlocfilehash: 4209b319e066d5481c669bcca021684f87532a3a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105793252"
---
# <a name="isearchitemgetparentfolder-method"></a><span data-ttu-id="89ec4-103">Método ISearchItem:: GetParentFolder</span><span class="sxs-lookup"><span data-stu-id="89ec4-103">ISearchItem::GetParentFolder method</span></span>

<span data-ttu-id="89ec4-104">Obtém o objeto [**ISearchItem**](-search-isearchitem.md) se a URL representa uma fonte de dados do Shell real (também conhecida como extensão de namespace do Shell).</span><span class="sxs-lookup"><span data-stu-id="89ec4-104">Gets the [**ISearchItem**](-search-isearchitem.md) object if the URL represents an actual Shell data source (also known as a Shell namespace extension).</span></span>

## <a name="syntax"></a><span data-ttu-id="89ec4-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="89ec4-105">Syntax</span></span>


```C++
HRESULT GetParentFolder(
  [out] ppShellFolder **IShellFolder,
  [out] ppidl         *LPITEMIDLIST
);
```



## <a name="parameters"></a><span data-ttu-id="89ec4-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="89ec4-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="89ec4-107">*IShellFolder* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="89ec4-107">*IShellFolder* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="89ec4-108">Tipo: **ppShellFolder \* \***</span><span class="sxs-lookup"><span data-stu-id="89ec4-108">Type: **ppShellFolder\*\***</span></span>

<span data-ttu-id="89ec4-109">No retorno, contém o endereço de um ponteiro para a pasta que contém a URL atual.</span><span class="sxs-lookup"><span data-stu-id="89ec4-109">On return, contains the address of a pointer to the folder that contains the current URL.</span></span> <span data-ttu-id="89ec4-110">A [interface IShellFolder](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellfolder) é exposta por todos os objetos de pasta de namespace do Shell, e seus métodos são usados para gerenciar pastas.</span><span class="sxs-lookup"><span data-stu-id="89ec4-110">[IShellFolder Interface](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellfolder) is exposed by all Shell namespace folder objects, and its methods are used to manage folders.</span></span>

</dd> <dt>

<span data-ttu-id="89ec4-111">*LPITEMIDLIST* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="89ec4-111">*LPITEMIDLIST* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="89ec4-112">Tipo: \**ppidl \** _</span><span class="sxs-lookup"><span data-stu-id="89ec4-112">Type: \**ppidl\** _</span></span>

<span data-ttu-id="89ec4-113">No retorno, contém o endereço de um ponteiro para uma lista de identificadores de item (PIDL) que identifica a pasta pai.</span><span class="sxs-lookup"><span data-stu-id="89ec4-113">On return, contains the address of a pointer to an item identifier list (PIDL) that identifies the parent folder.</span></span> <span data-ttu-id="89ec4-114">O parâmetro _LPITEMIDLIST \* pode se referir a um objeto em qualquer nível abaixo da pasta pai na hierarquia de namespace e, portanto, pode ser um ponteiro de vários níveis para um **PIDL** relativo à pasta pai.</span><span class="sxs-lookup"><span data-stu-id="89ec4-114">The _LPITEMIDLIST\* parameter can refer to an object at any level below the parent folder in the namespace hierarchy, and can thus be a multi-level pointer to a **pidl** relative to the parent folder.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="89ec4-115">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="89ec4-115">Return value</span></span>

<span data-ttu-id="89ec4-116">Tipo: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="89ec4-116">Type: **HRESULT**</span></span>

<span data-ttu-id="89ec4-117">Se esse método for bem sucedido, ele retornará **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="89ec4-117">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="89ec4-118">Caso contrário, ele retorna um código de erro **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="89ec4-118">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="89ec4-119">Comentários</span><span class="sxs-lookup"><span data-stu-id="89ec4-119">Remarks</span></span>

<span data-ttu-id="89ec4-120">O método **ISearchItem:: GetParentFolder** tem suporte apenas no Windows XP e no windows Server 2003 e não deve mais ser usado.</span><span class="sxs-lookup"><span data-stu-id="89ec4-120">The **ISearchItem::GetParentFolder** method is supported only on Windows XP and Windows Server 2003, and should no longer be used.</span></span>

<span data-ttu-id="89ec4-121">Para visualizar os anexos com um manipulador de protocolo de terceiros em computadores que executam o Windows XP ou o Windows Server 2003, pode ser necessário usar a interface [**ISearchItem**](-search-isearchitem.md) e as seguintes APIs: as interfaces [**IItemPreviewerExt**](-search-iitempreviewerext.md), [**IItemPropertyBag**](iitempropertybag.md)e [**ISearchProtocolUI**](-search-isearchprotocolui.md) , a estrutura [**LINKINFO**](-search-linkinfo.md) e a enumeração [**LinkId**](-search-linktype.md) .</span><span class="sxs-lookup"><span data-stu-id="89ec4-121">To preview attachments with a third-party protocol handler on computers running Windows XP or Windows Server 2003, it may be necessary to use the [**ISearchItem**](-search-isearchitem.md) interface, and the following APIs: the [**IItemPreviewerExt**](-search-iitempreviewerext.md), [**IItemPropertyBag**](iitempropertybag.md), and [**ISearchProtocolUI**](-search-isearchprotocolui.md) interfaces, the [**LINKINFO**](-search-linkinfo.md) structure, and the [**LINKTYPE**](-search-linktype.md) enumeration.</span></span>

## <a name="requirements"></a><span data-ttu-id="89ec4-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="89ec4-122">Requirements</span></span>



| <span data-ttu-id="89ec4-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="89ec4-123">Requirement</span></span> | <span data-ttu-id="89ec4-124">Valor</span><span class="sxs-lookup"><span data-stu-id="89ec4-124">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="89ec4-125">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="89ec4-125">Minimum supported client</span></span><br/> | <span data-ttu-id="89ec4-126">\[Somente aplicativos de área de trabalho do Windows XP com SP2\]</span><span class="sxs-lookup"><span data-stu-id="89ec4-126">Windows XP with SP2 \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="89ec4-127">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="89ec4-127">Minimum supported server</span></span><br/> | <span data-ttu-id="89ec4-128">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="89ec4-128">Windows Server 2003 \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="89ec4-129">Redistribuível</span><span class="sxs-lookup"><span data-stu-id="89ec4-129">Redistributable</span></span><br/>          | <span data-ttu-id="89ec4-130">Windows Desktop Search (WDS) 3,0</span><span class="sxs-lookup"><span data-stu-id="89ec4-130">Windows Desktop Search (WDS) 3.0</span></span><br/>          |



## <a name="see-also"></a><span data-ttu-id="89ec4-131">Confira também</span><span class="sxs-lookup"><span data-stu-id="89ec4-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="89ec4-132">**ISearchItem**</span><span class="sxs-lookup"><span data-stu-id="89ec4-132">**ISearchItem**</span></span>](-search-isearchitem.md)
</dt> </dl>

 

 
