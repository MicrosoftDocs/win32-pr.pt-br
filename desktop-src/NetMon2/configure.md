---
description: Configura o especialista no DLL especialista.
ms.assetid: 3906569d-9ad4-4c03-9637-f4a57697b227
title: Configurar função de retorno de chamada (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Configure
api_type:
- UserDefined
api_location:
- Netmon.h
ms.openlocfilehash: 76ba55b7544e35a07b74a41788a3befa766f87bc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105758296"
---
# <a name="configure-callback-function"></a><span data-ttu-id="46ae7-103">Configurar função de retorno de chamada</span><span class="sxs-lookup"><span data-stu-id="46ae7-103">Configure callback function</span></span>

<span data-ttu-id="46ae7-104">A função **Configurar** configura o especialista na DLL do especialista.</span><span class="sxs-lookup"><span data-stu-id="46ae7-104">The **Configure** function configures the expert within the expert DLL.</span></span>

<span data-ttu-id="46ae7-105">O especialista deve implementar a função **Configurar** .</span><span class="sxs-lookup"><span data-stu-id="46ae7-105">The expert must implement the **Configure** function.</span></span> <span data-ttu-id="46ae7-106">Quando a chamada de função é recebida, o especialista exibe uma caixa de diálogo que permite ao usuário alterar qualquer item configurável.</span><span class="sxs-lookup"><span data-stu-id="46ae7-106">When the function call is received, the expert displays a dialog box that enables the user to change any configurable item.</span></span>

## <a name="syntax"></a><span data-ttu-id="46ae7-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="46ae7-107">Syntax</span></span>


```C++
BOOL WINAPI Configure(
  _In_    HEXPERTKEY         hExpertKey,
  _Inout_ PEXPERTCONFIG      *ppConfig,
  _In_    PEXPERTSTARTUPINFO pExpertStartupInfo,
  _In_    DWORD              StartupFlags,
  _In_    HWND               hWnd
);
```



## <a name="parameters"></a><span data-ttu-id="46ae7-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="46ae7-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="46ae7-109">*hExpertKey* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="46ae7-109">*hExpertKey* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="46ae7-110">Identificador de especialista exclusivo.</span><span class="sxs-lookup"><span data-stu-id="46ae7-110">Unique expert identifier.</span></span>

<span data-ttu-id="46ae7-111">O identificador exclusivo é passado de volta em todas as funções de Monitor de Rede específicas do especialista.</span><span class="sxs-lookup"><span data-stu-id="46ae7-111">The unique identifier is passed back on all expert-specific Network Monitor functions.</span></span> <span data-ttu-id="46ae7-112">Lembre-se de que o identificador pode não ser a mesma chave de especialista que foi passada para a função de [**execução**](run.md) .</span><span class="sxs-lookup"><span data-stu-id="46ae7-112">Be aware that the identifier may not be the same expert key as the one passed to the [**Run**](run.md) function.</span></span> <span data-ttu-id="46ae7-113">Não armazene a chave de especialista da chamada de **configuração** .</span><span class="sxs-lookup"><span data-stu-id="46ae7-113">Do not store the expert key from the **Configure** call.</span></span>

</dd> <dt>

<span data-ttu-id="46ae7-114">*ppConfig* \[ entrada, saída\]</span><span class="sxs-lookup"><span data-stu-id="46ae7-114">*ppConfig* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="46ae7-115">Um ponteiro para um ponteiro para uma estrutura [**EXPERTCONFIG**](expertconfig.md) na entrada.</span><span class="sxs-lookup"><span data-stu-id="46ae7-115">A pointer to a pointer to an [**EXPERTCONFIG**](expertconfig.md) structure upon entry.</span></span>

<span data-ttu-id="46ae7-116">Após uma saída bem-sucedida, a estrutura [**EXPERTCONFIG**](expertconfig.md) referenciada contém os novos dados de configuração.</span><span class="sxs-lookup"><span data-stu-id="46ae7-116">After a successful exit, the referenced [**EXPERTCONFIG**](expertconfig.md) structure contains the new configuration data.</span></span>

</dd> <dt>

<span data-ttu-id="46ae7-117">*pExpertStartupInfo* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="46ae7-117">*pExpertStartupInfo* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="46ae7-118">Um ponteiro para o elemento capture com foco quando o especialista foi iniciado.</span><span class="sxs-lookup"><span data-stu-id="46ae7-118">A pointer to the capture element with focus when the expert started.</span></span>

</dd> <dt>

<span data-ttu-id="46ae7-119">*StartupFlags* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="46ae7-119">*StartupFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="46ae7-120">Os sinalizadores que indicam como o especialista deve usar o parâmetro *pExpertStartupInfo* .</span><span class="sxs-lookup"><span data-stu-id="46ae7-120">The flags that indicate how the expert should use the *pExpertStartupInfo* parameter.</span></span> <span data-ttu-id="46ae7-121">O único sinalizador definido é um **sinalizador de inicialização de especialista que \_ \_ \_ usa dados de \_ inicialização \_ \_ em \_ \_ dados de configuração**.</span><span class="sxs-lookup"><span data-stu-id="46ae7-121">The only flag defined is **EXPERT\_STARTUP\_FLAG\_USE\_STARTUP\_DATA\_OVER\_CONFIG\_DATA**.</span></span> <span data-ttu-id="46ae7-122">O sinalizador indica que o especialista usará o parâmetro *pExpertStartupInfo* em vez do parâmetro *ppConfig* que passou.</span><span class="sxs-lookup"><span data-stu-id="46ae7-122">The flag indicates that the expert will use the *pExpertStartupInfo* parameter rather than the *ppConfig* parameter that passed in.</span></span> <span data-ttu-id="46ae7-123">Normalmente, você define o sinalizador ao iniciar o especialista em um menu de contexto.</span><span class="sxs-lookup"><span data-stu-id="46ae7-123">Typically, you set the flag when you start the expert from a context menu.</span></span>

</dd> <dt>

<span data-ttu-id="46ae7-124">*HWND* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="46ae7-124">*hWnd* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="46ae7-125">Um identificador para a janela pai.</span><span class="sxs-lookup"><span data-stu-id="46ae7-125">A handle to the parent window.</span></span> <span data-ttu-id="46ae7-126">Use a alça para abrir uma caixa de diálogo.</span><span class="sxs-lookup"><span data-stu-id="46ae7-126">Use the handle to open a dialog box.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="46ae7-127">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="46ae7-127">Return value</span></span>

<span data-ttu-id="46ae7-128">Se a função for bem-sucedida (ou seja, se existir uma configuração atual), o valor de retorno será **true**.</span><span class="sxs-lookup"><span data-stu-id="46ae7-128">If the function is successful (that is, if a current configuration exists), the return value is **TRUE**.</span></span>

<span data-ttu-id="46ae7-129">Se a função não for bem-sucedida, o valor de retorno será **false**.</span><span class="sxs-lookup"><span data-stu-id="46ae7-129">If the function is unsuccessful, the return value is **FALSE**.</span></span>

## <a name="remarks"></a><span data-ttu-id="46ae7-130">Comentários</span><span class="sxs-lookup"><span data-stu-id="46ae7-130">Remarks</span></span>

<span data-ttu-id="46ae7-131">Monitor de Rede chama a função **Configurar** com a configuração atual do especialista, se houver.</span><span class="sxs-lookup"><span data-stu-id="46ae7-131">Network Monitor calls the **Configure** function with the current configuration of the expert, if one exists.</span></span> <span data-ttu-id="46ae7-132">O especialista exibe uma caixa de diálogo, com a qual você pode alterar qualquer item configurável.</span><span class="sxs-lookup"><span data-stu-id="46ae7-132">The expert displays a dialog box, with which you can change any configurable item.</span></span>

<span data-ttu-id="46ae7-133">Quando *ppConfig* é passado e monitor de rede não tem uma configuração armazenada para o especialista especificado, o valor do parâmetro pode ser **nulo**.</span><span class="sxs-lookup"><span data-stu-id="46ae7-133">When *ppConfig* is passed in and Network Monitor does not have a configuration stored for the specified expert, the parameter value can be **NULL**.</span></span> <span data-ttu-id="46ae7-134">Nesse caso, a função **Configure** pressupõe valores padrão embutidos em código (ou usa as informações de inicialização) para abrir a caixa de diálogo.</span><span class="sxs-lookup"><span data-stu-id="46ae7-134">In this case, the **Configure** function assumes hard-coded default values (or, uses the startup information) to open the dialog box.</span></span>

<span data-ttu-id="46ae7-135">Os dados de configuração também podem ser **nulos** quando a função **Configure** retorna, e um **NULL** foi passado.</span><span class="sxs-lookup"><span data-stu-id="46ae7-135">The configuration data can also be **NULL** when the **Configure** function returns, and a **NULL** was passed-in.</span></span> <span data-ttu-id="46ae7-136">Essa situação ocorre quando Monitor de Rede não tem um padrão armazenado e o usuário pressiona **Cancelar**.</span><span class="sxs-lookup"><span data-stu-id="46ae7-136">This situation occurs when Network Monitor does not have a stored default, and the user presses **Cancel**.</span></span>

<span data-ttu-id="46ae7-137">O início da estrutura de dados [**EXPERTCONFIG**](expertconfig.md) inclui uma seção privada que armazena as informações de tamanho da estrutura.</span><span class="sxs-lookup"><span data-stu-id="46ae7-137">The beginning of the [**EXPERTCONFIG**](expertconfig.md) data structure includes a Private section that stores the structure size information.</span></span> <span data-ttu-id="46ae7-138">O tamanho da estrutura **EXPERTCONFIG** deve incluir o comprimento de **DWORD** reservado que aparece no início da estrutura.</span><span class="sxs-lookup"><span data-stu-id="46ae7-138">The size of the **EXPERTCONFIG** structure should include the reserved **DWORD** length that appears at the beginning of the structure.</span></span> <span data-ttu-id="46ae7-139">Por exemplo, se os dados de configuração exigirem 20 bytes de espaço de armazenamento, aloque 24 bytes para armazenar os dados.</span><span class="sxs-lookup"><span data-stu-id="46ae7-139">For example, if your configuration data requires 20 bytes of storage space, allocate 24 bytes to store the data.</span></span> <span data-ttu-id="46ae7-140">Se um *ppConfig* for **nulo**, a função **Configure** chamará a função [**ExpertAllocMemory**](expertallocmemory.md) para alocar uma nova configuração com o tamanho correto.</span><span class="sxs-lookup"><span data-stu-id="46ae7-140">If a *ppConfig* is **NULL**, the **Configure** function calls the [**ExpertAllocMemory**](expertallocmemory.md) function to allocate a new configuration that is the correct size.</span></span> <span data-ttu-id="46ae7-141">Se o buffer não for suficiente para manter os dados de especialista, o especialista deverá chamar a função [**ExpertReallocMemory**](expertreallocmemory.md) .</span><span class="sxs-lookup"><span data-stu-id="46ae7-141">If the buffer is not enough to hold the expert data, the expert should call the [**ExpertReallocMemory**](expertreallocmemory.md) function.</span></span>

## <a name="requirements"></a><span data-ttu-id="46ae7-142">Requisitos</span><span class="sxs-lookup"><span data-stu-id="46ae7-142">Requirements</span></span>



| <span data-ttu-id="46ae7-143">Requisito</span><span class="sxs-lookup"><span data-stu-id="46ae7-143">Requirement</span></span> | <span data-ttu-id="46ae7-144">Valor</span><span class="sxs-lookup"><span data-stu-id="46ae7-144">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="46ae7-145">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="46ae7-145">Minimum supported client</span></span><br/> | <span data-ttu-id="46ae7-146">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="46ae7-146">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="46ae7-147">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="46ae7-147">Minimum supported server</span></span><br/> | <span data-ttu-id="46ae7-148">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="46ae7-148">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="46ae7-149">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="46ae7-149">Header</span></span><br/>                   | <dl> <span data-ttu-id="46ae7-150"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="46ae7-150"><dt>Netmon.h</dt></span></span> </dl> |



 

 




