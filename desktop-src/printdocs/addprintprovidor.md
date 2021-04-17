---
description: A função AddPrintProvidor instala um provedor de impressão local e vincula a configuração, os dados e os arquivos do provedor.
ms.assetid: f34549c3-0474-48ba-9307-5b36f02dbe1c
title: Função AddPrintProvidor (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- AddPrintProvidor
- AddPrintProvidorA
- AddPrintProvidorW
api_type:
- DllExport
api_location:
- Winspool.drv
ms.openlocfilehash: adf5f914046eb82e070e3e9915325989ff868d1e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105759521"
---
# <a name="addprintprovidor-function"></a><span data-ttu-id="4e382-103">Função AddPrintProvidor</span><span class="sxs-lookup"><span data-stu-id="4e382-103">AddPrintProvidor function</span></span>

<span data-ttu-id="4e382-104">A função **AddPrintProvidor** instala um provedor de impressão local e vincula a configuração, os dados e os arquivos do provedor.</span><span class="sxs-lookup"><span data-stu-id="4e382-104">The **AddPrintProvidor** function installs a local print provider and links the configuration, data, and provider files.</span></span>

## <a name="syntax"></a><span data-ttu-id="4e382-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="4e382-105">Syntax</span></span>


```C++
BOOL AddPrintProvidor(
  _In_ LPTSTR pName,
  _In_ DWORD  Level,
  _In_ LPBYTE pProviderInfo
);
```



## <a name="parameters"></a><span data-ttu-id="4e382-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="4e382-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4e382-107">*pname* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="4e382-107">*pName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4e382-108">Um ponteiro para uma cadeia de caracteres terminada em nulo que especifica o nome do servidor no qual o provedor deve ser instalado.</span><span class="sxs-lookup"><span data-stu-id="4e382-108">A pointer to a null-terminated string that specifies the name of the server on which the provider should be installed.</span></span> <span data-ttu-id="4e382-109">Para sistemas que dão suporte apenas à instalação local de provedores, esse parâmetro deve ser **nulo**.</span><span class="sxs-lookup"><span data-stu-id="4e382-109">For systems that only support local installation of providers, this parameter should be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="4e382-110">*Nível* \[ do no\]</span><span class="sxs-lookup"><span data-stu-id="4e382-110">*Level* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4e382-111">O nível da estrutura à qual *pProviderInfo* aponta.</span><span class="sxs-lookup"><span data-stu-id="4e382-111">The level of the structure to which *pProviderInfo* points.</span></span> <span data-ttu-id="4e382-112">Pode ser um dos seguintes.</span><span class="sxs-lookup"><span data-stu-id="4e382-112">It can be one of the following.</span></span>



| <span data-ttu-id="4e382-113">Valor</span><span class="sxs-lookup"><span data-stu-id="4e382-113">Value</span></span>                                                                                                | <span data-ttu-id="4e382-114">Significado</span><span class="sxs-lookup"><span data-stu-id="4e382-114">Meaning</span></span>                                                                            |
|------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------|
| <span id="1"></span><dl> <span data-ttu-id="4e382-115"><dt>**1**</dt></span><span class="sxs-lookup"><span data-stu-id="4e382-115"><dt>**1**</dt></span></span> </dl> | <span data-ttu-id="4e382-116">A função usa uma estrutura [**PROVIDOR \_ info \_ 1**](providor-info-1.md) .</span><span class="sxs-lookup"><span data-stu-id="4e382-116">Function uses a [**PROVIDOR\_INFO\_1**](providor-info-1.md) structure.</span></span><br/> |
| <span id="2"></span><dl> <span data-ttu-id="4e382-117"><dt>**2**</dt></span><span class="sxs-lookup"><span data-stu-id="4e382-117"><dt>**2**</dt></span></span> </dl> | <span data-ttu-id="4e382-118">A função usa uma estrutura [**PROVIDOR \_ info \_ 2**](providor-info-2.md) .</span><span class="sxs-lookup"><span data-stu-id="4e382-118">Function uses a [**PROVIDOR\_INFO\_2**](providor-info-2.md) structure.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="4e382-119">*pProviderInfo* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="4e382-119">*pProviderInfo* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4e382-120">Um ponteiro para uma estrutura de provedor de impressão, conforme indicado pelo *nível*.</span><span class="sxs-lookup"><span data-stu-id="4e382-120">A pointer to a print provider structure, as indicated by *Level*.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4e382-121">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="4e382-121">Return value</span></span>

<span data-ttu-id="4e382-122">Se a função for realizada com sucesso, o valor de retorno será um valor diferente de zero.</span><span class="sxs-lookup"><span data-stu-id="4e382-122">If the function succeeds, the return value is a nonzero value.</span></span>

<span data-ttu-id="4e382-123">Se a função falhar, o valor retornado será zero.</span><span class="sxs-lookup"><span data-stu-id="4e382-123">If the function fails, the return value is zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="4e382-124">Comentários</span><span class="sxs-lookup"><span data-stu-id="4e382-124">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="4e382-125">Essa é uma função de bloqueio ou síncrona e pode não retornar imediatamente.</span><span class="sxs-lookup"><span data-stu-id="4e382-125">This is a blocking or synchronous function and might not return immediately.</span></span> <span data-ttu-id="4e382-126">A rapidez com que essa função retorna depende de fatores de tempo de execução, como status de rede, configuração de servidor de impressão e fatores de implementação de driver de impressora que são difíceis de prever ao escrever um aplicativo.</span><span class="sxs-lookup"><span data-stu-id="4e382-126">How quickly this function returns depends on run-time factors such as network status, print server configuration, and printer driver implementation factors that are difficult to predict when writing an application.</span></span> <span data-ttu-id="4e382-127">Chamar essa função de um thread que gerencia a interação com a interface do usuário pode fazer com que o aplicativo pareça não responder.</span><span class="sxs-lookup"><span data-stu-id="4e382-127">Calling this function from a thread that manages interaction with the user interface could make the application appear to be unresponsive.</span></span>

 

<span data-ttu-id="4e382-128">Antes que um aplicativo chame a função **AddPrintProvidor** , todos os arquivos exigidos pelo provedor devem ser copiados para o diretório system32.</span><span class="sxs-lookup"><span data-stu-id="4e382-128">Before an application calls the **AddPrintProvidor** function, all files required by the provider must be copied to the SYSTEM32 directory.</span></span>

<span data-ttu-id="4e382-129">Um provedor adicionado pelo **AddPrintProvidor** pode ser removido chamando [**DeletePrintProvidor**](deleteprintprovidor.md).</span><span class="sxs-lookup"><span data-stu-id="4e382-129">A provider added by **AddPrintProvidor** may be removed by calling [**DeletePrintProvidor**](deleteprintprovidor.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="4e382-130">Requisitos</span><span class="sxs-lookup"><span data-stu-id="4e382-130">Requirements</span></span>



| <span data-ttu-id="4e382-131">Requisito</span><span class="sxs-lookup"><span data-stu-id="4e382-131">Requirement</span></span> | <span data-ttu-id="4e382-132">Valor</span><span class="sxs-lookup"><span data-stu-id="4e382-132">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4e382-133">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="4e382-133">Minimum supported client</span></span><br/> | <span data-ttu-id="4e382-134">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="4e382-134">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="4e382-135">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="4e382-135">Minimum supported server</span></span><br/> | <span data-ttu-id="4e382-136">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="4e382-136">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="4e382-137">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="4e382-137">Header</span></span><br/>                   | <dl> <span data-ttu-id="4e382-138"><dt>Winspool. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="4e382-138"><dt>Winspool.h (include Windows.h)</dt></span></span> </dl> |
| <span data-ttu-id="4e382-139">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="4e382-139">Library</span></span><br/>                  | <dl> <span data-ttu-id="4e382-140"><dt>Winspool. lib</dt></span><span class="sxs-lookup"><span data-stu-id="4e382-140"><dt>Winspool.lib</dt></span></span> </dl>                   |
| <span data-ttu-id="4e382-141">DLL</span><span class="sxs-lookup"><span data-stu-id="4e382-141">DLL</span></span><br/>                      | <dl> <span data-ttu-id="4e382-142"><dt>Winspool. drv</dt></span><span class="sxs-lookup"><span data-stu-id="4e382-142"><dt>Winspool.drv</dt></span></span> </dl>                   |
| <span data-ttu-id="4e382-143">Nomes Unicode e ANSI</span><span class="sxs-lookup"><span data-stu-id="4e382-143">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="4e382-144">**AddPrintProvidorW** (Unicode) e **AddPrintProvidorA** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="4e382-144">**AddPrintProvidorW** (Unicode) and **AddPrintProvidorA** (ANSI)</span></span><br/>                               |



## <a name="see-also"></a><span data-ttu-id="4e382-145">Confira também</span><span class="sxs-lookup"><span data-stu-id="4e382-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4e382-146">Impressão</span><span class="sxs-lookup"><span data-stu-id="4e382-146">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="4e382-147">Funções da API do Spooler de impressão</span><span class="sxs-lookup"><span data-stu-id="4e382-147">Print Spooler API Functions</span></span>](printing-and-print-spooler-functions.md)
</dt> <dt>

[<span data-ttu-id="4e382-148">**DeletePrintProvidor**</span><span class="sxs-lookup"><span data-stu-id="4e382-148">**DeletePrintProvidor**</span></span>](deleteprintprovidor.md)
</dt> <dt>

[<span data-ttu-id="4e382-149">**Informações de PROVIDOR \_ \_ 1**</span><span class="sxs-lookup"><span data-stu-id="4e382-149">**PROVIDOR\_INFO\_1**</span></span>](providor-info-1.md)
</dt> <dt>

[<span data-ttu-id="4e382-150">**Informações de PROVIDOR \_ \_ 2**</span><span class="sxs-lookup"><span data-stu-id="4e382-150">**PROVIDOR\_INFO\_2**</span></span>](providor-info-2.md)
</dt> </dl>

 

 




