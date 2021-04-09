---
description: A função SetPort define o status associado a uma porta de impressora.
ms.assetid: 1b80ad93-aaa1-41ed-a668-a944fa62c3eb
title: Função SetPort (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SetPort
- SetPortA
- SetPortW
api_type:
- DllExport
api_location:
- Winspool.drv
ms.openlocfilehash: ab986128c9561b7b95de668367cafb0b3e6cd636
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104010972"
---
# <a name="setport-function"></a><span data-ttu-id="e5230-103">Função SetPort</span><span class="sxs-lookup"><span data-stu-id="e5230-103">SetPort function</span></span>

<span data-ttu-id="e5230-104">A função **SetPort** define o status associado a uma porta de impressora.</span><span class="sxs-lookup"><span data-stu-id="e5230-104">The **SetPort** function sets the status associated with a printer port.</span></span>

## <a name="syntax"></a><span data-ttu-id="e5230-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="e5230-105">Syntax</span></span>


```C++
BOOL SetPort(
  _In_ LPTSTR pName,
  _In_ LPTSTR pPortName,
  _In_ DWORD  dwLevel,
  _In_ LPBYTE pPortInfo
);
```



## <a name="parameters"></a><span data-ttu-id="e5230-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="e5230-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e5230-107">*pname* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="e5230-107">*pName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e5230-108">Ponteiro para uma cadeia de caracteres terminada em zero que especifica o nome do servidor de impressora ao qual a porta está conectada.</span><span class="sxs-lookup"><span data-stu-id="e5230-108">Pointer to a zero-terminated string that specifies the name of the printer server to which the port is connected.</span></span> <span data-ttu-id="e5230-109">Defina esse parâmetro como **NULL** se a porta estiver no computador local.</span><span class="sxs-lookup"><span data-stu-id="e5230-109">Set this parameter to **NULL** if the port is on the local machine.</span></span>

</dd> <dt>

<span data-ttu-id="e5230-110">*pPortName* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="e5230-110">*pPortName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e5230-111">Ponteiro para uma cadeia de caracteres terminada em zero que especifica o nome da porta da impressora.</span><span class="sxs-lookup"><span data-stu-id="e5230-111">Pointer to a zero-terminated string that specifies the name of the printer port.</span></span>

</dd> <dt>

<span data-ttu-id="e5230-112">*dwLevel* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="e5230-112">*dwLevel* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e5230-113">Especifica o tipo de estrutura apontado pelo parâmetro *pPortInfo* .</span><span class="sxs-lookup"><span data-stu-id="e5230-113">Specifies the type of structure pointed to by the *pPortInfo* parameter.</span></span>

<span data-ttu-id="e5230-114">Esse valor deve ser 3, que corresponde a uma estrutura de dados de [**informações de porta \_ \_ 3**](port-info-3.md) .</span><span class="sxs-lookup"><span data-stu-id="e5230-114">This value must be 3, which corresponds to a [**PORT\_INFO\_3**](port-info-3.md) data structure.</span></span>

</dd> <dt>

<span data-ttu-id="e5230-115">*pPortInfo* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="e5230-115">*pPortInfo* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e5230-116">Ponteiro para uma estrutura de [**informações de porta \_ \_ 3**](port-info-3.md) que contém as informações de status da porta a serem definidas.</span><span class="sxs-lookup"><span data-stu-id="e5230-116">Pointer to a [**PORT\_INFO\_3**](port-info-3.md) structure that contains the port status information to set.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e5230-117">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="e5230-117">Return value</span></span>

<span data-ttu-id="e5230-118">Se a função for realizada com sucesso, o valor de retorno será um valor diferente de zero.</span><span class="sxs-lookup"><span data-stu-id="e5230-118">If the function succeeds, the return value is a nonzero value.</span></span>

<span data-ttu-id="e5230-119">Se a função falhar, o valor retornado será zero.</span><span class="sxs-lookup"><span data-stu-id="e5230-119">If the function fails, the return value is zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="e5230-120">Comentários</span><span class="sxs-lookup"><span data-stu-id="e5230-120">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="e5230-121">Essa é uma função de bloqueio ou síncrona e pode não retornar imediatamente.</span><span class="sxs-lookup"><span data-stu-id="e5230-121">This is a blocking or synchronous function and might not return immediately.</span></span> <span data-ttu-id="e5230-122">A rapidez com que essa função retorna depende de fatores de tempo de execução, como status de rede, configuração de servidor de impressão e fatores de implementação de driver de impressora que são difíceis de prever ao escrever um aplicativo.</span><span class="sxs-lookup"><span data-stu-id="e5230-122">How quickly this function returns depends on run-time factors such as network status, print server configuration, and printer driver implementation factors that are difficult to predict when writing an application.</span></span> <span data-ttu-id="e5230-123">Chamar essa função de um thread que gerencia a interação com a interface do usuário pode fazer com que o aplicativo pareça não responder.</span><span class="sxs-lookup"><span data-stu-id="e5230-123">Calling this function from a thread that manages interaction with the user interface could make the application appear to be unresponsive.</span></span>

 

<span data-ttu-id="e5230-124">O chamador da função **SetPort** deve ser executado como administrador.</span><span class="sxs-lookup"><span data-stu-id="e5230-124">The caller of the **SetPort** function must be executing as an Administrator.</span></span> <span data-ttu-id="e5230-125">Além disso, se o chamador for um monitor de porta ou monitor de idioma, ele deverá chamar [**RevertToSelf**](/windows/desktop/api/securitybaseapi/nf-securitybaseapi-reverttoself) para interromper a representação antes de chamar **SetPort**.</span><span class="sxs-lookup"><span data-stu-id="e5230-125">Additionally, if the caller is a Port Monitor or Language Monitor, it must call [**RevertToSelf**](/windows/desktop/api/securitybaseapi/nf-securitybaseapi-reverttoself) to cease impersonation before it calls **SetPort**.</span></span>

<span data-ttu-id="e5230-126">Todos os programas que chamam **SetPort** devem ter \_ acesso de servidor \_ para administrar o acesso ao servidor ao qual a porta está conectada.</span><span class="sxs-lookup"><span data-stu-id="e5230-126">All programs that call **SetPort** must have SERVER\_ACCESS\_ADMINISTER access to the server to which the port is connected.</span></span>

<span data-ttu-id="e5230-127">Quando você define um valor de status de porta de impressora com o valor de severidade \_ erro de tipo de status \_ \_ , o spooler de impressão para de enviar trabalhos para a porta.</span><span class="sxs-lookup"><span data-stu-id="e5230-127">When you set a printer port status value with the severity value PORT\_STATUS\_TYPE\_ERROR, the print spooler stops sending jobs to the port.</span></span> <span data-ttu-id="e5230-128">O spooler de impressão retoma o envio de trabalhos para a porta quando o status da porta é limpo por outra chamada para **SetPort**.</span><span class="sxs-lookup"><span data-stu-id="e5230-128">The print spooler resumes sending jobs to the port when the port status is cleared by another call to **SetPort**.</span></span>

## <a name="requirements"></a><span data-ttu-id="e5230-129">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e5230-129">Requirements</span></span>



| <span data-ttu-id="e5230-130">Requisito</span><span class="sxs-lookup"><span data-stu-id="e5230-130">Requirement</span></span> | <span data-ttu-id="e5230-131">Valor</span><span class="sxs-lookup"><span data-stu-id="e5230-131">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e5230-132">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="e5230-132">Minimum supported client</span></span><br/> | <span data-ttu-id="e5230-133">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="e5230-133">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="e5230-134">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="e5230-134">Minimum supported server</span></span><br/> | <span data-ttu-id="e5230-135">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="e5230-135">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="e5230-136">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="e5230-136">Header</span></span><br/>                   | <dl> <span data-ttu-id="e5230-137"><dt>Winspool. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="e5230-137"><dt>Winspool.h (include Windows.h)</dt></span></span> </dl> |
| <span data-ttu-id="e5230-138">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="e5230-138">Library</span></span><br/>                  | <dl> <span data-ttu-id="e5230-139"><dt>Winspool. lib</dt></span><span class="sxs-lookup"><span data-stu-id="e5230-139"><dt>Winspool.lib</dt></span></span> </dl>                   |
| <span data-ttu-id="e5230-140">DLL</span><span class="sxs-lookup"><span data-stu-id="e5230-140">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e5230-141"><dt>Winspool. drv</dt></span><span class="sxs-lookup"><span data-stu-id="e5230-141"><dt>Winspool.drv</dt></span></span> </dl>                   |
| <span data-ttu-id="e5230-142">Nomes Unicode e ANSI</span><span class="sxs-lookup"><span data-stu-id="e5230-142">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="e5230-143">**SetPortW** (Unicode) e **setportaa** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="e5230-143">**SetPortW** (Unicode) and **SetPortA** (ANSI)</span></span><br/>                                                 |



## <a name="see-also"></a><span data-ttu-id="e5230-144">Confira também</span><span class="sxs-lookup"><span data-stu-id="e5230-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e5230-145">Impressão</span><span class="sxs-lookup"><span data-stu-id="e5230-145">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="e5230-146">Funções da API do Spooler de impressão</span><span class="sxs-lookup"><span data-stu-id="e5230-146">Print Spooler API Functions</span></span>](printing-and-print-spooler-functions.md)
</dt> <dt>

[<span data-ttu-id="e5230-147">**Informações da porta \_ \_ 3**</span><span class="sxs-lookup"><span data-stu-id="e5230-147">**PORT\_INFO\_3**</span></span>](port-info-3.md)
</dt> </dl>

 

