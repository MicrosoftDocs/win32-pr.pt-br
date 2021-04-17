---
description: O método ProvideIntegerData do objeto ConfigureModule é chamado por Mergemod.dll para recuperar dados inteiros da ferramenta de cliente.
ms.assetid: 13d48301-bd63-432c-b663-85a840886dda
title: Método ConfigureModule. ProvideIntegerData (Mergemod. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ConfigureModule
- IMsmConfigureModule
api_type:
- COM
api_location:
- Mergemod.dll
ms.openlocfilehash: 482e1010dea850506b159b129eb4dcef77829fca
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105757127"
---
# <a name="configuremoduleprovideintegerdata-method"></a><span data-ttu-id="be7c2-103">Método ConfigureModule. ProvideIntegerData</span><span class="sxs-lookup"><span data-stu-id="be7c2-103">ConfigureModule.ProvideIntegerData method</span></span>

<span data-ttu-id="be7c2-104">O método **ProvideIntegerData** do [**objeto ConfigureModule**](configuremodule-object.md) é chamado por Mergemod.dll para recuperar dados inteiros da ferramenta de cliente.</span><span class="sxs-lookup"><span data-stu-id="be7c2-104">The **ProvideIntegerData** method of the [**ConfigureModule object**](configuremodule-object.md) is called by Mergemod.dll to retrieve integer data from the client tool.</span></span>

<span data-ttu-id="be7c2-105">Mergemod.dll fornece o *nome* da entrada correspondente na [Tabela ModuleConfiguration](moduleconfiguration-table.md).</span><span class="sxs-lookup"><span data-stu-id="be7c2-105">Mergemod.dll provides the *Name* from the corresponding entry in the [ModuleConfiguration table](moduleconfiguration-table.md).</span></span>

<span data-ttu-id="be7c2-106">A ferramenta deve retornar S \_ OK e fornecer o inteiro de personalização apropriado em *ConfigData*.</span><span class="sxs-lookup"><span data-stu-id="be7c2-106">The tool should return S\_OK and provide the appropriate customization integer in *ConfigData*.</span></span>

<span data-ttu-id="be7c2-107">Se a ferramenta não fornecer dados de configuração para esse valor de *nome* , a função deverá retornar S \_ false.</span><span class="sxs-lookup"><span data-stu-id="be7c2-107">If the tool does not provide any configuration data for this *Name* value, the function should return S\_FALSE.</span></span> <span data-ttu-id="be7c2-108">Nesse caso Mergemod.dll ignora o valor do argumento *ConfigData* e usa o valor padrão da Tabela ModuleConfiguration.</span><span class="sxs-lookup"><span data-stu-id="be7c2-108">In this case Mergemod.dll ignores the value of the *ConfigData* argument and uses the Default value from the ModuleConfiguration table.</span></span>

## <a name="syntax"></a><span data-ttu-id="be7c2-109">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="be7c2-109">Syntax</span></span>


```JScript
ConfigureModule.ProvideIntegerData(
  Name,
  ConfigData
)
```



## <a name="parameters"></a><span data-ttu-id="be7c2-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="be7c2-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="be7c2-111">*Nome*</span><span class="sxs-lookup"><span data-stu-id="be7c2-111">*Name*</span></span> 
</dt> <dd>

<span data-ttu-id="be7c2-112">Nome do item para o qual os dados estão sendo recuperados.</span><span class="sxs-lookup"><span data-stu-id="be7c2-112">Name of item for which data is being retrieved.</span></span>

</dd> <dt>

<span data-ttu-id="be7c2-113">*ConfigData*</span><span class="sxs-lookup"><span data-stu-id="be7c2-113">*ConfigData*</span></span> 
</dt> <dd>

<span data-ttu-id="be7c2-114">Ponteiro para texto de personalização.</span><span class="sxs-lookup"><span data-stu-id="be7c2-114">Pointer to customization text.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="be7c2-115">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="be7c2-115">Return value</span></span>

<span data-ttu-id="be7c2-116">Esse método não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="be7c2-116">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="be7c2-117">Comentários</span><span class="sxs-lookup"><span data-stu-id="be7c2-117">Remarks</span></span>

<span data-ttu-id="be7c2-118">O cliente pode ser chamado não mais de uma vez para cada registro na [Tabela ModuleConfiguration](moduleconfiguration-table.md).</span><span class="sxs-lookup"><span data-stu-id="be7c2-118">The client may be called no more than once for each record in the [ModuleConfiguration table](moduleconfiguration-table.md).</span></span> <span data-ttu-id="be7c2-119">Observe que Mergemod.dll nunca faz várias chamadas para o cliente para o mesmo valor de "nome".</span><span class="sxs-lookup"><span data-stu-id="be7c2-119">Note that Mergemod.dll never makes multiple calls to the client for the same "Name" value.</span></span> <span data-ttu-id="be7c2-120">Se nenhum registro na tabela ModuleSubstitution usar a propriedade, uma entrada na Tabela ModuleConfiguration não fará chamadas para o cliente.</span><span class="sxs-lookup"><span data-stu-id="be7c2-120">If no record in the ModuleSubstitution table uses the property, an entry in the ModuleConfiguration table causes no calls to the client.</span></span>

### <a name="c"></a><span data-ttu-id="be7c2-121">C++</span><span class="sxs-lookup"><span data-stu-id="be7c2-121">C++</span></span>

<span data-ttu-id="be7c2-122">Consulte a [**função ProvideIntegerData**](/windows/desktop/api/Mergemod/nf-mergemod-imsmconfiguremodule-provideintegerdata).</span><span class="sxs-lookup"><span data-stu-id="be7c2-122">See [**ProvideIntegerData function**](/windows/desktop/api/Mergemod/nf-mergemod-imsmconfiguremodule-provideintegerdata).</span></span>

## <a name="requirements"></a><span data-ttu-id="be7c2-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="be7c2-123">Requirements</span></span>



| <span data-ttu-id="be7c2-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="be7c2-124">Requirement</span></span> | <span data-ttu-id="be7c2-125">Valor</span><span class="sxs-lookup"><span data-stu-id="be7c2-125">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="be7c2-126">Versão</span><span class="sxs-lookup"><span data-stu-id="be7c2-126">Version</span></span><br/> | <span data-ttu-id="be7c2-127">Mergemod.dll 2,0 ou posterior</span><span class="sxs-lookup"><span data-stu-id="be7c2-127">Mergemod.dll 2.0 or later</span></span><br/>                                                    |
| <span data-ttu-id="be7c2-128">parâmetro</span><span class="sxs-lookup"><span data-stu-id="be7c2-128">Header</span></span><br/>  | <dl> <span data-ttu-id="be7c2-129"><dt>Mergemod. h</dt></span><span class="sxs-lookup"><span data-stu-id="be7c2-129"><dt>Mergemod.h</dt></span></span> </dl>   |
| <span data-ttu-id="be7c2-130">DLL</span><span class="sxs-lookup"><span data-stu-id="be7c2-130">DLL</span></span><br/>     | <dl> <span data-ttu-id="be7c2-131"><dt>Mergemod.dll</dt></span><span class="sxs-lookup"><span data-stu-id="be7c2-131"><dt>Mergemod.dll</dt></span></span> </dl> |



 

 




