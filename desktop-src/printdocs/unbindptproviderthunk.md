---
description: Fecha um identificador para um provedor de tíquete de impressão.
ms.assetid: ce979c89-9f9d-4e89-b142-beed414caa3f
title: Função UnbindPTProviderThunk
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- UnbindPTProviderThunk
api_type:
- DllExport
api_location:
- prntvpt.dll
ms.openlocfilehash: dd87f528603624e9957d8c5f3fb12cc857ec4f5a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105764020"
---
# <a name="unbindptproviderthunk-function"></a><span data-ttu-id="3debe-103">Função UnbindPTProviderThunk</span><span class="sxs-lookup"><span data-stu-id="3debe-103">UnbindPTProviderThunk function</span></span>

<span data-ttu-id="3debe-104">\[Essa função não tem suporte e pode ser desabilitada ou excluída em versões futuras do Windows.</span><span class="sxs-lookup"><span data-stu-id="3debe-104">\[This function is not supported and might be disabled or deleted in future versions of Windows.</span></span> <span data-ttu-id="3debe-105">O [**PTCloseProvider**](/windows/desktop/api/prntvpt/nf-prntvpt-ptcloseprovider) fornece funcionalidade equivalente e deve ser usado em vez disso.\]</span><span class="sxs-lookup"><span data-stu-id="3debe-105">[**PTCloseProvider**](/windows/desktop/api/prntvpt/nf-prntvpt-ptcloseprovider) provides equivalent functionality and should be used instead.\]</span></span>

<span data-ttu-id="3debe-106">Fecha um identificador para um provedor de tíquete de impressão.</span><span class="sxs-lookup"><span data-stu-id="3debe-106">Closes a handle to a print ticket provider.</span></span>

## <a name="syntax"></a><span data-ttu-id="3debe-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="3debe-107">Syntax</span></span>


```C++
HRESULT UnbindPTProviderThunk(
  _In_ HPTPROVIDER hProvider
);
```



## <a name="parameters"></a><span data-ttu-id="3debe-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="3debe-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3debe-109">*hProvider* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="3debe-109">*hProvider* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3debe-110">Um identificador para um provedor de tíquete de impressão aberto.</span><span class="sxs-lookup"><span data-stu-id="3debe-110">A handle to an open print ticket provider.</span></span> <span data-ttu-id="3debe-111">Esse identificador é retornado pela função [**BindPTProviderThunk**](bindptproviderthunk.md) .</span><span class="sxs-lookup"><span data-stu-id="3debe-111">This handle is returned by the [**BindPTProviderThunk**](bindptproviderthunk.md) function.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3debe-112">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="3debe-112">Return value</span></span>

<span data-ttu-id="3debe-113">Se o método for bem sucedido, ele retornará **S \_ OK**; caso contrário, ele retornará um código de erro **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="3debe-113">If the method succeeds, it returns **S\_OK**; otherwise, it returns an **HRESULT** error code.</span></span> <span data-ttu-id="3debe-114">Para obter mais informações sobre códigos de erro COM, consulte [tratamento de erros](../com/error-handling-in-com.md).</span><span class="sxs-lookup"><span data-stu-id="3debe-114">For more information about COM error codes, see [Error Handling](../com/error-handling-in-com.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="3debe-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3debe-115">Requirements</span></span>



| <span data-ttu-id="3debe-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="3debe-116">Requirement</span></span> | <span data-ttu-id="3debe-117">Valor</span><span class="sxs-lookup"><span data-stu-id="3debe-117">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="3debe-118">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="3debe-118">Minimum supported client</span></span><br/> | <span data-ttu-id="3debe-119">\[Somente aplicativos da área de trabalho do Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="3debe-119">Windows XP \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="3debe-120">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="3debe-120">Minimum supported server</span></span><br/> | <span data-ttu-id="3debe-121">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="3debe-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="3debe-122">DLL</span><span class="sxs-lookup"><span data-stu-id="3debe-122">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3debe-123"><dt>Prntvpt.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3debe-123"><dt>Prntvpt.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3debe-124">Confira também</span><span class="sxs-lookup"><span data-stu-id="3debe-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3debe-125">Imprimir esquema</span><span class="sxs-lookup"><span data-stu-id="3debe-125">Print Schema</span></span>](./printschema.md)
</dt> <dt>

[<span data-ttu-id="3debe-126">**PTCloseProvider**</span><span class="sxs-lookup"><span data-stu-id="3debe-126">**PTCloseProvider**</span></span>](/windows/desktop/api/prntvpt/nf-prntvpt-ptcloseprovider)
</dt> <dt>

[<span data-ttu-id="3debe-127">Impressão</span><span class="sxs-lookup"><span data-stu-id="3debe-127">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="3debe-128">Funções da API do Spooler de impressão</span><span class="sxs-lookup"><span data-stu-id="3debe-128">Print Spooler API Functions</span></span>](printing-and-print-spooler-functions.md)
</dt> </dl>

 

