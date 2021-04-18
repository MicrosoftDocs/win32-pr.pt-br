---
description: O método ProvideTextData é chamado pelo Mergemod.dll para recuperar dados de texto da ferramenta de cliente. Mergemod.dll fornece o nome da entrada correspondente na Tabela ModuleConfiguration.
ms.assetid: 286b0b58-1b6a-4d41-89e1-eb9c23bdd788
title: Método ConfigureModule. ProvideTextData (Mergemod. h)
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
ms.openlocfilehash: 6801cb4b3ff90cb277d13573fe4527e8d76bfe0d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105752661"
---
# <a name="configuremoduleprovidetextdata-method"></a><span data-ttu-id="36397-104">Método ConfigureModule. ProvideTextData</span><span class="sxs-lookup"><span data-stu-id="36397-104">ConfigureModule.ProvideTextData method</span></span>

<span data-ttu-id="36397-105">O método **ProvideTextData** é chamado pelo Mergemod.dll para recuperar dados de texto da ferramenta de cliente.</span><span class="sxs-lookup"><span data-stu-id="36397-105">The **ProvideTextData** method is called by Mergemod.dll to retrieve text data from the client tool.</span></span> <span data-ttu-id="36397-106">Mergemod.dll fornece o *nome* da entrada correspondente na Tabela ModuleConfiguration.</span><span class="sxs-lookup"><span data-stu-id="36397-106">Mergemod.dll provides the *Name* from the corresponding entry in the ModuleConfiguration table.</span></span>

<span data-ttu-id="36397-107">A ferramenta deve retornar S \_ OK e fornecer o texto de personalização apropriado em ConfigData.</span><span class="sxs-lookup"><span data-stu-id="36397-107">The tool should return S\_OK and provide the appropriate customization text in ConfigData.</span></span> <span data-ttu-id="36397-108">A ferramenta de cliente é responsável por alocar os dados, mas Mergemod.dllé responsável por liberar a memória.</span><span class="sxs-lookup"><span data-stu-id="36397-108">The client tool is responsible for allocating the data, but Mergemod.dllis responsible for releasing the memory.</span></span> <span data-ttu-id="36397-109">Esse argumento deve ser um objeto **BSTR** .</span><span class="sxs-lookup"><span data-stu-id="36397-109">This argument MUST be a **BSTR** object.</span></span> <span data-ttu-id="36397-110">**LPCWSTR** não é aceito.</span><span class="sxs-lookup"><span data-stu-id="36397-110">**LPCWSTR** is NOT accepted.</span></span>

<span data-ttu-id="36397-111">Se a ferramenta não fornecer dados de configuração para esse valor de *nome* , a função deverá retornar S \_ false.</span><span class="sxs-lookup"><span data-stu-id="36397-111">If the tool does not provide any configuration data for this *Name* value, the function should return S\_FALSE.</span></span> <span data-ttu-id="36397-112">Nesse caso Mergemod.dll ignora o valor do argumento ConfigData e usa o valor padrão da Tabela ModuleConfiguration.</span><span class="sxs-lookup"><span data-stu-id="36397-112">In this case Mergemod.dll ignores the value of the ConfigData argument and uses the Default value from the ModuleConfiguration table.</span></span>

<span data-ttu-id="36397-113">Qualquer código de retorno diferente de S \_ OK ou s \_ false fará com que um erro seja registrado (se um log estiver aberto) e resultará na falha da mesclagem.</span><span class="sxs-lookup"><span data-stu-id="36397-113">Any return code other than S\_OK or S\_FALSE will cause an error to be logged (if a log is open) and will result in the merge failing.</span></span>

<span data-ttu-id="36397-114">Como essa função segue a convenção padrão **BSTR** , NULL é equivalente à cadeia de caracteres vazia.</span><span class="sxs-lookup"><span data-stu-id="36397-114">Because this function follows standard **BSTR** convention, null is equivalent to the empty string.</span></span>

## <a name="syntax"></a><span data-ttu-id="36397-115">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="36397-115">Syntax</span></span>


```JScript
ConfigureModule.ProvideTextData(
  Name,
  ConfigData
)
```



## <a name="parameters"></a><span data-ttu-id="36397-116">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="36397-116">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="36397-117">*Nome*</span><span class="sxs-lookup"><span data-stu-id="36397-117">*Name*</span></span> 
</dt> <dd>

<span data-ttu-id="36397-118">Nome do item para o qual os dados estão sendo recuperados.</span><span class="sxs-lookup"><span data-stu-id="36397-118">Name of item for which data is being retrieved.</span></span>

</dd> <dt>

<span data-ttu-id="36397-119">*ConfigData*</span><span class="sxs-lookup"><span data-stu-id="36397-119">*ConfigData*</span></span> 
</dt> <dd>

<span data-ttu-id="36397-120">Ponteiro para texto de personalização.</span><span class="sxs-lookup"><span data-stu-id="36397-120">Pointer to customization text.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="36397-121">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="36397-121">Return value</span></span>

<span data-ttu-id="36397-122">Esse método não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="36397-122">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="36397-123">Comentários</span><span class="sxs-lookup"><span data-stu-id="36397-123">Remarks</span></span>

<span data-ttu-id="36397-124">O cliente pode ser chamado não mais de uma vez para cada registro na [Tabela ModuleConfiguration](moduleconfiguration-table.md).</span><span class="sxs-lookup"><span data-stu-id="36397-124">The client may be called no more than once for each record in the [ModuleConfiguration table](moduleconfiguration-table.md).</span></span> <span data-ttu-id="36397-125">Observe que Mergemod.dll nunca faz várias chamadas para o cliente para o mesmo valor de "nome".</span><span class="sxs-lookup"><span data-stu-id="36397-125">Note that Mergemod.dll never makes multiple calls to the client for the same "Name" value.</span></span> <span data-ttu-id="36397-126">Se nenhum registro na tabela ModuleSubstitution usar a propriedade, uma entrada na Tabela ModuleConfiguration não fará chamadas para o cliente.</span><span class="sxs-lookup"><span data-stu-id="36397-126">If no record in the ModuleSubstitution table uses the property, an entry in the ModuleConfiguration table causes no calls to the client.</span></span>

### <a name="c"></a><span data-ttu-id="36397-127">C++</span><span class="sxs-lookup"><span data-stu-id="36397-127">C++</span></span>

<span data-ttu-id="36397-128">Consulte a [**função ProvideTextData**](/windows/desktop/api/Mergemod/nf-mergemod-imsmconfiguremodule-providetextdata).</span><span class="sxs-lookup"><span data-stu-id="36397-128">See [**ProvideTextData function**](/windows/desktop/api/Mergemod/nf-mergemod-imsmconfiguremodule-providetextdata).</span></span>

## <a name="requirements"></a><span data-ttu-id="36397-129">Requisitos</span><span class="sxs-lookup"><span data-stu-id="36397-129">Requirements</span></span>



| <span data-ttu-id="36397-130">Requisito</span><span class="sxs-lookup"><span data-stu-id="36397-130">Requirement</span></span> | <span data-ttu-id="36397-131">Valor</span><span class="sxs-lookup"><span data-stu-id="36397-131">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="36397-132">Versão</span><span class="sxs-lookup"><span data-stu-id="36397-132">Version</span></span><br/> | <span data-ttu-id="36397-133">Mergemod.dll 2,0 ou posterior</span><span class="sxs-lookup"><span data-stu-id="36397-133">Mergemod.dll 2.0 or later</span></span><br/>                                                    |
| <span data-ttu-id="36397-134">parâmetro</span><span class="sxs-lookup"><span data-stu-id="36397-134">Header</span></span><br/>  | <dl> <span data-ttu-id="36397-135"><dt>Mergemod. h</dt></span><span class="sxs-lookup"><span data-stu-id="36397-135"><dt>Mergemod.h</dt></span></span> </dl>   |
| <span data-ttu-id="36397-136">DLL</span><span class="sxs-lookup"><span data-stu-id="36397-136">DLL</span></span><br/>     | <dl> <span data-ttu-id="36397-137"><dt>Mergemod.dll</dt></span><span class="sxs-lookup"><span data-stu-id="36397-137"><dt>Mergemod.dll</dt></span></span> </dl> |



 

 




