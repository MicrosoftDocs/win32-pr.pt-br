---
description: O especialista deve implementar a função Run. Monitor de Rede chama a função executar para iniciar o especialista na DLL do especialista.
ms.assetid: 9ef3941b-d9e9-4acb-97ed-5f39573f2946
title: Executar função de retorno de chamada (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Run
api_type:
- UserDefined
api_location:
- Netmon.h
ms.openlocfilehash: c2dff2cf70a6d989928f17447fa3491dd9509f24
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103827279"
---
# <a name="run-callback-function"></a><span data-ttu-id="09478-104">Executar função de retorno de chamada</span><span class="sxs-lookup"><span data-stu-id="09478-104">Run callback function</span></span>

<span data-ttu-id="09478-105">O especialista deve implementar a função **Run** .</span><span class="sxs-lookup"><span data-stu-id="09478-105">The expert must implement the **Run** function.</span></span> <span data-ttu-id="09478-106">Monitor de Rede chama a função **executar** para iniciar o especialista na DLL do especialista.</span><span class="sxs-lookup"><span data-stu-id="09478-106">Network Monitor calls the **Run** function to start the expert within the expert DLL.</span></span>

## <a name="syntax"></a><span data-ttu-id="09478-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="09478-107">Syntax</span></span>


```C++
BOOL WINAPI Run(
  _In_ HEXPERTKEY         hExpertKey,
  _In_ PEXPERTCONFIG      pConfig,
  _In_ PEXPERTSTARTUPINFO pExpertStartupInfo,
  _In_ DWORD              StartupFlags,
  _In_ HWND               hWndParent
);
```



## <a name="parameters"></a><span data-ttu-id="09478-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="09478-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="09478-109">*hExpertKey* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="09478-109">*hExpertKey* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="09478-110">Identificador exclusivo do especialista que é passado de volta para todas as funções de Monitor de Rede específicas do especialista.</span><span class="sxs-lookup"><span data-stu-id="09478-110">Unique identifier of the expert that is passed back to all expert-specific Network Monitor functions.</span></span>

> [!Note]  
> <span data-ttu-id="09478-111">O identificador *hExpertKey* pode passar uma chave de especialista diferente da chave de especialista que a função [**Configurar**](configure.md) passa.</span><span class="sxs-lookup"><span data-stu-id="09478-111">The *hExpertKey* identifier may pass an expert key that is different from the expert key that the [**Configure**](configure.md) function passes.</span></span>

 

</dd> <dt>

<span data-ttu-id="09478-112">*pConfig* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="09478-112">*pConfig* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="09478-113">Ponteiro para a configuração existente.</span><span class="sxs-lookup"><span data-stu-id="09478-113">Pointer to the existing configuration.</span></span> <span data-ttu-id="09478-114">O parâmetro *pConfig* pode ser **nulo** , o que significa que o especialista pode ser executado com padrões embutidos em código ou informações de inicialização às quais o parâmetro *pExpertStartupInfo* faz referência.</span><span class="sxs-lookup"><span data-stu-id="09478-114">The *pConfig* parameter may be **NULL** which means that the expert can run with hard-coded defaults, or startup information that the *pExpertStartupInfo* parameter references.</span></span>

</dd> <dt>

<span data-ttu-id="09478-115">*pExpertStartupInfo* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="09478-115">*pExpertStartupInfo* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="09478-116">Ponteiro para o elemento capture que tem o foco quando o especialista é iniciado.</span><span class="sxs-lookup"><span data-stu-id="09478-116">Pointer to the capture element that has focus when the expert starts.</span></span>

</dd> <dt>

<span data-ttu-id="09478-117">*StartupFlags* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="09478-117">*StartupFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="09478-118">Indicador de como o especialista deve usar o parâmetro *pExpertStartupInfo* .</span><span class="sxs-lookup"><span data-stu-id="09478-118">Indicator for how the expert should use the *pExpertStartupInfo* parameter.</span></span>

<span data-ttu-id="09478-119">O único sinalizador definido é:</span><span class="sxs-lookup"><span data-stu-id="09478-119">The only flag defined is:</span></span>



| <span data-ttu-id="09478-120">Valor</span><span class="sxs-lookup"><span data-stu-id="09478-120">Value</span></span>                                                                                                                                                                                                                                                                                           | <span data-ttu-id="09478-121">Significado</span><span class="sxs-lookup"><span data-stu-id="09478-121">Meaning</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                       |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="EXPERT_STARTUP_FLAG_USE_STARTUP_DATA_OVER_CONFIG_DATA."></span><span id="expert_startup_flag_use_startup_data_over_config_data."></span><dl> <span data-ttu-id="09478-122"><dt>**sinalizador de inicialização de especialista \_ \_ \_ use \_ dados de inicialização \_ \_ em \_ dados de configuração \_ .**</dt></span><span class="sxs-lookup"><span data-stu-id="09478-122"><dt>**EXPERT\_STARTUP\_FLAG\_USE\_STARTUP\_DATA\_OVER\_CONFIG\_DATA.**</dt></span></span> </dl> | <span data-ttu-id="09478-123">Esse sinalizador indica que o especialista usa o parâmetro *pExpertStartupInfo* e não usa o parâmetro *pConfig* .</span><span class="sxs-lookup"><span data-stu-id="09478-123">This flag indicates that the expert uses the *pExpertStartupInfo* parameter, and does not use the *pConfig* parameter.</span></span> <span data-ttu-id="09478-124">Normalmente, você pode definir esse sinalizador quando o especialista puder iniciar a partir de um clique com o botão direito do mouse.</span><span class="sxs-lookup"><span data-stu-id="09478-124">Typically, you can set this flag when the expert can start from a right-mouse click.</span></span> <span data-ttu-id="09478-125">Se o sinalizador não estiver definido, as duas ações a seguir podem ocorrer: ou o especialista não começa com um clique com o botão direito do mouse, ou o especialista começa com um clique com o botão direito do mouse e o configura.</span><span class="sxs-lookup"><span data-stu-id="09478-125">If the flag is not set, the following two things can occur: either the expert does not start from a right-mouse click, or the expert starts from a right-mouse click, and then the user configures it.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="09478-126">*hwndParent* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="09478-126">*hWndParent* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="09478-127">O parâmetro *HWND* do pai (geralmente a interface do usuário monitor de rede).</span><span class="sxs-lookup"><span data-stu-id="09478-127">The *hWnd* parameter of the parent (usually the Network Monitor user interface).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="09478-128">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="09478-128">Return value</span></span>

<span data-ttu-id="09478-129">Se a função for bem-sucedida (ou seja, se o especialista for iniciado), o valor de retorno será **true**.</span><span class="sxs-lookup"><span data-stu-id="09478-129">If the function is successful (that is, if the expert starts), the return value is **TRUE**.</span></span>

<span data-ttu-id="09478-130">Se a função não for bem-sucedida, o valor de retorno será **false**.</span><span class="sxs-lookup"><span data-stu-id="09478-130">If the function is unsuccessful, the return value is **FALSE**.</span></span>

## <a name="remarks"></a><span data-ttu-id="09478-131">Comentários</span><span class="sxs-lookup"><span data-stu-id="09478-131">Remarks</span></span>

<span data-ttu-id="09478-132">Durante a execução, o especialista percorre os quadros no arquivo de captura e gera um relatório ou cria eventos que mostram problemas.</span><span class="sxs-lookup"><span data-stu-id="09478-132">When running, the expert loops through the frames in the capture file and either generates a report or creates events that show problems.</span></span>

## <a name="requirements"></a><span data-ttu-id="09478-133">Requisitos</span><span class="sxs-lookup"><span data-stu-id="09478-133">Requirements</span></span>



| <span data-ttu-id="09478-134">Requisito</span><span class="sxs-lookup"><span data-stu-id="09478-134">Requirement</span></span> | <span data-ttu-id="09478-135">Valor</span><span class="sxs-lookup"><span data-stu-id="09478-135">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="09478-136">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="09478-136">Minimum supported client</span></span><br/> | <span data-ttu-id="09478-137">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="09478-137">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="09478-138">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="09478-138">Minimum supported server</span></span><br/> | <span data-ttu-id="09478-139">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="09478-139">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="09478-140">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="09478-140">Header</span></span><br/>                   | <dl> <span data-ttu-id="09478-141"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="09478-141"><dt>Netmon.h</dt></span></span> </dl> |



 

 




