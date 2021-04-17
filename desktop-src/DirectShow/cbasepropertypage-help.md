---
description: 'O método Help invoca a ajuda da página de propriedades. Esse método implementa o método IPropertyPage:: help.'
ms.assetid: 8fe72b2e-a9f1-435d-8eda-27056f112c6d
title: Método CBasePropertyPage. Help (cProp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBasePropertyPage.Help
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: b87c8ba76928fbf0e465a8b6a3a0aaf4730759f1
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105811756"
---
# <a name="cbasepropertypagehelp-method"></a><span data-ttu-id="5b0fd-104">Método CBasePropertyPage. Help</span><span class="sxs-lookup"><span data-stu-id="5b0fd-104">CBasePropertyPage.Help method</span></span>

<span data-ttu-id="5b0fd-105">O `Help` método invoca a ajuda da página de propriedades.</span><span class="sxs-lookup"><span data-stu-id="5b0fd-105">The `Help` method invokes the property page help.</span></span> <span data-ttu-id="5b0fd-106">Esse método implementa o método **IPropertyPage:: help** .</span><span class="sxs-lookup"><span data-stu-id="5b0fd-106">This method implements the **IPropertyPage::Help** method.</span></span>

## <a name="syntax"></a><span data-ttu-id="5b0fd-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="5b0fd-107">Syntax</span></span>


```C++
HRESULT Help(
   LPCWSTR lpszHelpDir
);
```



## <a name="parameters"></a><span data-ttu-id="5b0fd-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="5b0fd-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5b0fd-109">*lpszHelpDir*</span><span class="sxs-lookup"><span data-stu-id="5b0fd-109">*lpszHelpDir*</span></span> 
</dt> <dd>

<span data-ttu-id="5b0fd-110">Ponteiro para a cadeia de caracteres sob a chave **HelpDir** nas informações de CLSID da página de propriedades no registro.</span><span class="sxs-lookup"><span data-stu-id="5b0fd-110">Pointer to the string under the **HelpDir** key in the property page's CLSID information in the registry.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5b0fd-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="5b0fd-111">Return value</span></span>

<span data-ttu-id="5b0fd-112">Retorna E \_ NOTIMPL.</span><span class="sxs-lookup"><span data-stu-id="5b0fd-112">Returns E\_NOTIMPL.</span></span>

## <a name="remarks"></a><span data-ttu-id="5b0fd-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="5b0fd-113">Remarks</span></span>

<span data-ttu-id="5b0fd-114">Na classe base, o método sempre retorna E \_ NOTIMPL.</span><span class="sxs-lookup"><span data-stu-id="5b0fd-114">In the base class, the method always returns E\_NOTIMPL.</span></span> <span data-ttu-id="5b0fd-115">Quando o método falha, o quadro chama **IPropertyPage:: GetPageInfo** para obter o nome do arquivo de ajuda e o identificador de contexto.</span><span class="sxs-lookup"><span data-stu-id="5b0fd-115">When the method fails, the frame calls **IPropertyPage::GetPageInfo** to get the name of the help file and context identifier.</span></span> <span data-ttu-id="5b0fd-116">Por padrão, elas são **nulas**.</span><span class="sxs-lookup"><span data-stu-id="5b0fd-116">By default, these are **NULL**.</span></span> <span data-ttu-id="5b0fd-117">Para fornecer ajuda, portanto, a classe derivada pode substituir o método `Help` ou o método [**CBasePropertyPage:: GetPageInfo**](cbasepropertypage-getpageinfo.md) .</span><span class="sxs-lookup"><span data-stu-id="5b0fd-117">To provide help, therefore, the derived class can override either the `Help` method or the [**CBasePropertyPage::GetPageInfo**](cbasepropertypage-getpageinfo.md) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="5b0fd-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5b0fd-118">Requirements</span></span>



| <span data-ttu-id="5b0fd-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="5b0fd-119">Requirement</span></span> | <span data-ttu-id="5b0fd-120">Valor</span><span class="sxs-lookup"><span data-stu-id="5b0fd-120">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5b0fd-121">parâmetro</span><span class="sxs-lookup"><span data-stu-id="5b0fd-121">Header</span></span><br/>  | <dl> <span data-ttu-id="5b0fd-122"><dt>CProp. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="5b0fd-122"><dt>Cprop.h (include Streams.h)</dt></span></span> </dl>                                                                                     |
| <span data-ttu-id="5b0fd-123">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="5b0fd-123">Library</span></span><br/> | <dl> <span data-ttu-id="5b0fd-124"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="5b0fd-124"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5b0fd-125">Confira também</span><span class="sxs-lookup"><span data-stu-id="5b0fd-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5b0fd-126">**Classe CBasePropertyPage**</span><span class="sxs-lookup"><span data-stu-id="5b0fd-126">**CBasePropertyPage Class**</span></span>](cbasepropertypage.md)
</dt> </dl>

 

 




