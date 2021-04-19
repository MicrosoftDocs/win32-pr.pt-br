---
description: A função DeletePrinterDriver remove o nome de driver de impressora especificado da lista de nomes de drivers com suporte em um servidor.
ms.assetid: b159bd8b-3416-44a5-91bf-c0447ed6b465
title: Função DeletePrinterDriver (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DeletePrinterDriver
- DeletePrinterDriverA
- DeletePrinterDriverW
api_type:
- DllExport
api_location:
- Winspool.drv
ms.openlocfilehash: 9e84730be0d20100c2da42aa357f35c08cfb0727
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105748362"
---
# <a name="deleteprinterdriver-function"></a><span data-ttu-id="c2f2c-103">Função DeletePrinterDriver</span><span class="sxs-lookup"><span data-stu-id="c2f2c-103">DeletePrinterDriver function</span></span>

<span data-ttu-id="c2f2c-104">A função **DeletePrinterDriver** remove o nome de driver de impressora especificado da lista de nomes de drivers com suporte em um servidor.</span><span class="sxs-lookup"><span data-stu-id="c2f2c-104">The **DeletePrinterDriver** function removes the specified printer-driver name from the list of names of supported drivers on a server.</span></span>

<span data-ttu-id="c2f2c-105">Para excluir os arquivos associados ao driver, além de remover o nome de driver de impressora especificado da lista de nomes de drivers com suporte para um servidor, use a função [**DeletePrinterDriverEx**](deleteprinterdriverex.md) .</span><span class="sxs-lookup"><span data-stu-id="c2f2c-105">To delete the files associated with the driver in addition to removing the specified printer-driver name from the list of names of supported drivers for a server, use the [**DeletePrinterDriverEx**](deleteprinterdriverex.md) function.</span></span>

<span data-ttu-id="c2f2c-106">**DeletePrinterDriver** excluirá um driver somente se nenhuma versão do driver estiver em uso para o ambiente especificado.</span><span class="sxs-lookup"><span data-stu-id="c2f2c-106">**DeletePrinterDriver** deletes a driver only if no version of the driver is in use for the specified environment.</span></span> <span data-ttu-id="c2f2c-107">[**DeletePrinterDriverEx**](deleteprinterdriverex.md) pode excluir versões específicas do driver.</span><span class="sxs-lookup"><span data-stu-id="c2f2c-107">[**DeletePrinterDriverEx**](deleteprinterdriverex.md) can delete specific versions of the driver.</span></span>

## <a name="syntax"></a><span data-ttu-id="c2f2c-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="c2f2c-108">Syntax</span></span>


```C++
BOOL DeletePrinterDriver(
  _In_ LPTSTR pName,
  _In_ LPTSTR pEnvironment,
  _In_ LPTSTR pDriverName
);
```



## <a name="parameters"></a><span data-ttu-id="c2f2c-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="c2f2c-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c2f2c-110">*pname* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="c2f2c-110">*pName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c2f2c-111">Um ponteiro para uma cadeia de caracteres terminada em nulo que especifica o nome do servidor do qual o driver deve ser excluído.</span><span class="sxs-lookup"><span data-stu-id="c2f2c-111">A pointer to a null-terminated string that specifies the name of the server from which the driver is to be deleted.</span></span> <span data-ttu-id="c2f2c-112">Se esse parâmetro for **nulo**, o nome do driver de impressora será removido localmente.</span><span class="sxs-lookup"><span data-stu-id="c2f2c-112">If this parameter is **NULL**, the printer-driver name will be removed locally.</span></span>

</dd> <dt>

<span data-ttu-id="c2f2c-113">*pEnvironment* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="c2f2c-113">*pEnvironment* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c2f2c-114">Um ponteiro para uma cadeia de caracteres terminada em nulo que especifica o ambiente do qual o driver deve ser excluído (por exemplo, Windows x86, Windows IA64 ou Windows x64).</span><span class="sxs-lookup"><span data-stu-id="c2f2c-114">A pointer to a null-terminated string that specifies the environment from which the driver is to be deleted (for example, Windows x86, Windows IA64, or Windows x64).</span></span> <span data-ttu-id="c2f2c-115">Se esse parâmetro for **nulo**, o nome do driver será excluído do ambiente atual do aplicativo de chamada e do computador cliente (não do aplicativo de destino e do servidor de impressão).</span><span class="sxs-lookup"><span data-stu-id="c2f2c-115">If this parameter is **NULL**, the driver name is deleted from the current environment of the calling application and client machine (not of the destination application and print server).</span></span>

</dd> <dt>

<span data-ttu-id="c2f2c-116">*pDriverName* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="c2f2c-116">*pDriverName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c2f2c-117">Um ponteiro para uma cadeia de caracteres terminada em nulo que especifica o nome do driver que deve ser excluído.</span><span class="sxs-lookup"><span data-stu-id="c2f2c-117">A pointer to a null-terminated string specifying the name of the driver that should be deleted.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c2f2c-118">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="c2f2c-118">Return value</span></span>

<span data-ttu-id="c2f2c-119">Se a função for realizada com sucesso, o valor de retorno será um valor diferente de zero.</span><span class="sxs-lookup"><span data-stu-id="c2f2c-119">If the function succeeds, the return value is a nonzero value.</span></span>

<span data-ttu-id="c2f2c-120">Se a função falhar, o valor retornado será zero.</span><span class="sxs-lookup"><span data-stu-id="c2f2c-120">If the function fails, the return value is zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="c2f2c-121">Comentários</span><span class="sxs-lookup"><span data-stu-id="c2f2c-121">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="c2f2c-122">Essa é uma função de bloqueio ou síncrona e pode não retornar imediatamente.</span><span class="sxs-lookup"><span data-stu-id="c2f2c-122">This is a blocking or synchronous function and might not return immediately.</span></span> <span data-ttu-id="c2f2c-123">A rapidez com que essa função retorna depende de fatores de tempo de execução, como status de rede, configuração de servidor de impressão e fatores de implementação de driver de impressora que são difíceis de prever ao escrever um aplicativo.</span><span class="sxs-lookup"><span data-stu-id="c2f2c-123">How quickly this function returns depends on run-time factors such as network status, print server configuration, and printer driver implementation factors that are difficult to predict when writing an application.</span></span> <span data-ttu-id="c2f2c-124">Chamar essa função de um thread que gerencia a interação com a interface do usuário pode fazer com que o aplicativo pareça não responder.</span><span class="sxs-lookup"><span data-stu-id="c2f2c-124">Calling this function from a thread that manages interaction with the user interface could make the application appear to be unresponsive.</span></span>

 

<span data-ttu-id="c2f2c-125">O chamador deve ter o [SeLoadDriverPrivilege](/windows/desktop/SecAuthZ/authorization-constants).</span><span class="sxs-lookup"><span data-stu-id="c2f2c-125">The caller must have the [SeLoadDriverPrivilege](/windows/desktop/SecAuthZ/authorization-constants).</span></span>

<span data-ttu-id="c2f2c-126">A função **DeletePrinterDriver** não exclui os arquivos associados, ele simplesmente remove o nome do driver da lista retornada pela função [**EnumPrinterDrivers**](enumprinterdrivers.md) .</span><span class="sxs-lookup"><span data-stu-id="c2f2c-126">The **DeletePrinterDriver** function does not delete the associated files, it merely removes the driver name from the list returned by the [**EnumPrinterDrivers**](enumprinterdrivers.md) function.</span></span>

<span data-ttu-id="c2f2c-127">Antes de chamar **DeletePrinterDriver**, você deve excluir todos os objetos de impressora que usam o driver de impressora.</span><span class="sxs-lookup"><span data-stu-id="c2f2c-127">Before calling **DeletePrinterDriver**, you must delete all printer objects that use the printer driver.</span></span>

## <a name="requirements"></a><span data-ttu-id="c2f2c-128">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c2f2c-128">Requirements</span></span>



| <span data-ttu-id="c2f2c-129">Requisito</span><span class="sxs-lookup"><span data-stu-id="c2f2c-129">Requirement</span></span> | <span data-ttu-id="c2f2c-130">Valor</span><span class="sxs-lookup"><span data-stu-id="c2f2c-130">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c2f2c-131">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="c2f2c-131">Minimum supported client</span></span><br/> | <span data-ttu-id="c2f2c-132">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="c2f2c-132">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="c2f2c-133">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="c2f2c-133">Minimum supported server</span></span><br/> | <span data-ttu-id="c2f2c-134">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="c2f2c-134">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="c2f2c-135">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="c2f2c-135">Header</span></span><br/>                   | <dl> <span data-ttu-id="c2f2c-136"><dt>Winspool. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="c2f2c-136"><dt>Winspool.h (include Windows.h)</dt></span></span> </dl> |
| <span data-ttu-id="c2f2c-137">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="c2f2c-137">Library</span></span><br/>                  | <dl> <span data-ttu-id="c2f2c-138"><dt>Winspool. lib</dt></span><span class="sxs-lookup"><span data-stu-id="c2f2c-138"><dt>Winspool.lib</dt></span></span> </dl>                   |
| <span data-ttu-id="c2f2c-139">DLL</span><span class="sxs-lookup"><span data-stu-id="c2f2c-139">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c2f2c-140"><dt>Winspool. drv</dt></span><span class="sxs-lookup"><span data-stu-id="c2f2c-140"><dt>Winspool.drv</dt></span></span> </dl>                   |
| <span data-ttu-id="c2f2c-141">Nomes Unicode e ANSI</span><span class="sxs-lookup"><span data-stu-id="c2f2c-141">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="c2f2c-142">**DeletePrinterDriverW** (Unicode) e **DeletePrinterDriverA** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="c2f2c-142">**DeletePrinterDriverW** (Unicode) and **DeletePrinterDriverA** (ANSI)</span></span><br/>                         |



## <a name="see-also"></a><span data-ttu-id="c2f2c-143">Confira também</span><span class="sxs-lookup"><span data-stu-id="c2f2c-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c2f2c-144">Impressão</span><span class="sxs-lookup"><span data-stu-id="c2f2c-144">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="c2f2c-145">Funções da API do Spooler de impressão</span><span class="sxs-lookup"><span data-stu-id="c2f2c-145">Print Spooler API Functions</span></span>](printing-and-print-spooler-functions.md)
</dt> <dt>

[<span data-ttu-id="c2f2c-146">**DeletePrinterDriverEx**</span><span class="sxs-lookup"><span data-stu-id="c2f2c-146">**DeletePrinterDriverEx**</span></span>](deleteprinterdriverex.md)
</dt> <dt>

[<span data-ttu-id="c2f2c-147">**EnumPrinterDrivers**</span><span class="sxs-lookup"><span data-stu-id="c2f2c-147">**EnumPrinterDrivers**</span></span>](enumprinterdrivers.md)
</dt> </dl>

 

