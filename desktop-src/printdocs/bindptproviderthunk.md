---
description: Abre uma instância de um provedor de tíquete de impressão.
ms.assetid: 815cc360-8dcd-4c58-a64d-5d77436a8623
title: Função BindPTProviderThunk
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- BindPTProviderThunk
api_type:
- DllExport
api_location:
- prntvpt.dll
ms.openlocfilehash: bf63fc6faf9d47993fafb97c8d3a1c18d6d6c985
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104169352"
---
# <a name="bindptproviderthunk-function"></a><span data-ttu-id="77ae2-103">Função BindPTProviderThunk</span><span class="sxs-lookup"><span data-stu-id="77ae2-103">BindPTProviderThunk function</span></span>

<span data-ttu-id="77ae2-104">\[Essa função não tem suporte e pode ser desabilitada ou excluída em versões futuras do Windows.</span><span class="sxs-lookup"><span data-stu-id="77ae2-104">\[This function is not supported and might be disabled or deleted in future versions of Windows.</span></span> <span data-ttu-id="77ae2-105">O [**PTOpenProviderEx**](/windows/desktop/api/prntvpt/nf-prntvpt-ptopenproviderex) fornece funcionalidade equivalente e deve ser usado em vez disso.\]</span><span class="sxs-lookup"><span data-stu-id="77ae2-105">[**PTOpenProviderEx**](/windows/desktop/api/prntvpt/nf-prntvpt-ptopenproviderex) provides equivalent functionality and should be used instead.\]</span></span>

<span data-ttu-id="77ae2-106">Abre uma instância de um provedor de tíquete de impressão.</span><span class="sxs-lookup"><span data-stu-id="77ae2-106">Opens an instance of a print ticket provider.</span></span>

## <a name="syntax"></a><span data-ttu-id="77ae2-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="77ae2-107">Syntax</span></span>


```C++
HRESULT BindPTProviderThunk(
  _In_  LPTSTR      pszPrinterName,
  _In_  INT         maxVersion,
  _In_  INT         prefVersion,
  _Out_ HPTPROVIDER *phProvider,
  _Out_ INT         *usedVersion
);
```



## <a name="parameters"></a><span data-ttu-id="77ae2-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="77ae2-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="77ae2-109">*pszPrinterName* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="77ae2-109">*pszPrinterName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="77ae2-110">O nome completo de uma fila de impressão.</span><span class="sxs-lookup"><span data-stu-id="77ae2-110">The full name of a print queue.</span></span>

</dd> <dt>

<span data-ttu-id="77ae2-111">*MaxVersion* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="77ae2-111">*maxVersion* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="77ae2-112">A versão mais recente do [esquema de impressão](./printschema.md) que o chamador dá suporte.</span><span class="sxs-lookup"><span data-stu-id="77ae2-112">The latest version of the [Print Schema](./printschema.md) that the caller supports.</span></span>

</dd> <dt>

<span data-ttu-id="77ae2-113">*prefVersion* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="77ae2-113">*prefVersion* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="77ae2-114">A versão do [esquema de impressão](./printschema.md) solicitado pelo chamador.</span><span class="sxs-lookup"><span data-stu-id="77ae2-114">The version of the [Print Schema](./printschema.md) requested by the caller.</span></span>

</dd> <dt>

<span data-ttu-id="77ae2-115">*phProvider* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="77ae2-115">*phProvider* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="77ae2-116">Um ponteiro para um identificador para o provedor de tíquete de impressão.</span><span class="sxs-lookup"><span data-stu-id="77ae2-116">A pointer to a handle to the print ticket provider.</span></span>

</dd> <dt>

<span data-ttu-id="77ae2-117">*usedVersion* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="77ae2-117">*usedVersion* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="77ae2-118">A versão do [esquema de impressão](./printschema.md) que o provedor de tíquete de impressão usará.</span><span class="sxs-lookup"><span data-stu-id="77ae2-118">The version of the [Print Schema](./printschema.md) that the print ticket provider will use.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="77ae2-119">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="77ae2-119">Return value</span></span>

<span data-ttu-id="77ae2-120">Se o método for bem sucedido, ele retornará **S \_ OK**; caso contrário, ele retornará um código de erro **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="77ae2-120">If the method succeeds, it returns **S\_OK**; otherwise, it returns an **HRESULT** error code.</span></span> <span data-ttu-id="77ae2-121">Para obter mais informações sobre códigos de erro COM, consulte [tratamento de erros](../com/error-handling-in-com.md).</span><span class="sxs-lookup"><span data-stu-id="77ae2-121">For more information about COM error codes, see [Error Handling](../com/error-handling-in-com.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="77ae2-122">Comentários</span><span class="sxs-lookup"><span data-stu-id="77ae2-122">Remarks</span></span>

<span data-ttu-id="77ae2-123">Antes de chamar essa função, o thread de chamada deve inicializar COM chamando [**CoInitializeEx**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializeex).</span><span class="sxs-lookup"><span data-stu-id="77ae2-123">Before calling this function, the calling thread must initialize COM by calling [**CoInitializeEx**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializeex).</span></span>

## <a name="requirements"></a><span data-ttu-id="77ae2-124">Requisitos</span><span class="sxs-lookup"><span data-stu-id="77ae2-124">Requirements</span></span>



| <span data-ttu-id="77ae2-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="77ae2-125">Requirement</span></span> | <span data-ttu-id="77ae2-126">Valor</span><span class="sxs-lookup"><span data-stu-id="77ae2-126">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="77ae2-127">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="77ae2-127">Minimum supported client</span></span><br/> | <span data-ttu-id="77ae2-128">\[Somente aplicativos da área de trabalho do Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="77ae2-128">Windows XP \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="77ae2-129">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="77ae2-129">Minimum supported server</span></span><br/> | <span data-ttu-id="77ae2-130">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="77ae2-130">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="77ae2-131">DLL</span><span class="sxs-lookup"><span data-stu-id="77ae2-131">DLL</span></span><br/>                      | <dl> <span data-ttu-id="77ae2-132"><dt>Prntvpt.dll</dt></span><span class="sxs-lookup"><span data-stu-id="77ae2-132"><dt>Prntvpt.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="77ae2-133">Confira também</span><span class="sxs-lookup"><span data-stu-id="77ae2-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="77ae2-134">Imprimir esquema</span><span class="sxs-lookup"><span data-stu-id="77ae2-134">Print Schema</span></span>](./printschema.md)
</dt> <dt>

[<span data-ttu-id="77ae2-135">**PTOpenProviderEx**</span><span class="sxs-lookup"><span data-stu-id="77ae2-135">**PTOpenProviderEx**</span></span>](/windows/desktop/api/prntvpt/nf-prntvpt-ptopenproviderex)
</dt> <dt>

[<span data-ttu-id="77ae2-136">Impressão</span><span class="sxs-lookup"><span data-stu-id="77ae2-136">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="77ae2-137">Funções da API do Spooler de impressão</span><span class="sxs-lookup"><span data-stu-id="77ae2-137">Print Spooler API Functions</span></span>](printing-and-print-spooler-functions.md)
</dt> </dl>

 

