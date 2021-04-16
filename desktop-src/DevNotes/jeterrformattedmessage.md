---
description: Recupera um IDA (identificador de código de erro) e cria a cadeia de caracteres de exibição final quando um erro de Jet e informações de erro estendidas são fornecidas.
ms.assetid: 961da4fb-cb70-4f3d-a4a4-1774be7a05f4
title: Função JetErrFormattedMessage
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- JetErrFormattedMessage
api_type:
- DllExport
api_location:
- Msjter40.dll
ms.openlocfilehash: 75cdf93b4c35a8c7b3dd77fca42c205d898f6e97
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105747676"
---
# <a name="jeterrformattedmessage-function"></a><span data-ttu-id="6ec88-103">Função JetErrFormattedMessage</span><span class="sxs-lookup"><span data-stu-id="6ec88-103">JetErrFormattedMessage function</span></span>

<span data-ttu-id="6ec88-104">Recupera um IDA (identificador de código de erro) e cria a cadeia de caracteres de exibição final quando um erro de Jet e informações de erro estendidas são fornecidas.</span><span class="sxs-lookup"><span data-stu-id="6ec88-104">Retrieves an error code identifier (IDA) and creates the final display string when a Jet error and extended error information is provided.</span></span>

## <a name="syntax"></a><span data-ttu-id="6ec88-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="6ec88-105">Syntax</span></span>


```C++
JET_ERR JetErrFormattedMessage(
   JET_ERR              err,
   JETERR_EXTERR        *pExtendedErrorInfo,
   JETERR_IDA           *pIda,
   WCHAR                *pMessage,
   unsigned long        cbMessage,
   unsigned long        *pcbActual,
   JETERR_HELPCONTEXTID *pContextId,
   WCHAR                **pwszHelp/file
);
```



## <a name="parameters"></a><span data-ttu-id="6ec88-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="6ec88-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6ec88-107">*erra*</span><span class="sxs-lookup"><span data-stu-id="6ec88-107">*err*</span></span> 
</dt> <dd>

<span data-ttu-id="6ec88-108">O número do erro Jet que é usado para pesquisar e formatar a mensagem de erro exibível.</span><span class="sxs-lookup"><span data-stu-id="6ec88-108">The Jet error number that is used to look up and format the displayable error message.</span></span>

</dd> <dt>

<span data-ttu-id="6ec88-109">*pExtendedErrorInfo*</span><span class="sxs-lookup"><span data-stu-id="6ec88-109">*pExtendedErrorInfo*</span></span> 
</dt> <dd>

<span data-ttu-id="6ec88-110">Todas as informações de erro do Jet, incluindo o nome do banco de dados, o nome da tabela e qualquer informação de erro secundária.</span><span class="sxs-lookup"><span data-stu-id="6ec88-110">All Jet error information including the database name, the table name, and any minor error information.</span></span>

</dd> <dt>

<span data-ttu-id="6ec88-111">*pIda*</span><span class="sxs-lookup"><span data-stu-id="6ec88-111">*pIda*</span></span> 
</dt> <dd>

<span data-ttu-id="6ec88-112">Um ponteiro para o IDA que está associado ao código de erro específico.</span><span class="sxs-lookup"><span data-stu-id="6ec88-112">A pointer to the IDA that is associated with the specific error code.</span></span>

</dd> <dt>

<span data-ttu-id="6ec88-113">*pMessage*</span><span class="sxs-lookup"><span data-stu-id="6ec88-113">*pMessage*</span></span> 
</dt> <dd>

<span data-ttu-id="6ec88-114">Um ponteiro para a mensagem de erro.</span><span class="sxs-lookup"><span data-stu-id="6ec88-114">A pointer to the error message.</span></span>

</dd> <dt>

<span data-ttu-id="6ec88-115">*cbMessage*</span><span class="sxs-lookup"><span data-stu-id="6ec88-115">*cbMessage*</span></span> 
</dt> <dd>

<span data-ttu-id="6ec88-116">Uma contagem do número de bytes na mensagem de erro.</span><span class="sxs-lookup"><span data-stu-id="6ec88-116">A count of the number of bytes in the error message.</span></span>

</dd> <dt>

<span data-ttu-id="6ec88-117">*pcbActual*</span><span class="sxs-lookup"><span data-stu-id="6ec88-117">*pcbActual*</span></span> 
</dt> <dd>

<span data-ttu-id="6ec88-118">Um ponteiro para o número real de bytes lidos.</span><span class="sxs-lookup"><span data-stu-id="6ec88-118">A pointer to the actual number of bytes read.</span></span>

</dd> <dt>

<span data-ttu-id="6ec88-119">*pContextId*</span><span class="sxs-lookup"><span data-stu-id="6ec88-119">*pContextId*</span></span> 
</dt> <dd>

<span data-ttu-id="6ec88-120">Um ponteiro para o identificador de contexto associado ao arquivo de ajuda.</span><span class="sxs-lookup"><span data-stu-id="6ec88-120">A pointer to the context identifier that is associated with the help file.</span></span>

</dd> <dt>

<span data-ttu-id="6ec88-121">*pwszHelp/arquivo*</span><span class="sxs-lookup"><span data-stu-id="6ec88-121">*pwszHelp/file*</span></span> 
</dt> <dd>

<span data-ttu-id="6ec88-122">Um ponteiro para um ponteiro para o arquivo que explica o erro.</span><span class="sxs-lookup"><span data-stu-id="6ec88-122">A pointer to a pointer to the file that explains the error.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6ec88-123">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="6ec88-123">Return value</span></span>

<span data-ttu-id="6ec88-124">Se a função for realizada com êxito, ela retornará **Jet \_ errSuccess**; caso contrário, ela retornará uma mensagem de erro formatada que indica o motivo específico da falha.</span><span class="sxs-lookup"><span data-stu-id="6ec88-124">If the function succeeds, it returns **JET\_errSuccess**; otherwise, it returns a formatted error message that indicates the specific reason for failure.</span></span>

## <a name="remarks"></a><span data-ttu-id="6ec88-125">Comentários</span><span class="sxs-lookup"><span data-stu-id="6ec88-125">Remarks</span></span>

<span data-ttu-id="6ec88-126">Esta função não tem biblioteca de importação ou arquivo de cabeçalho associado; Você deve chamá-lo usando as funções [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) e [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) .</span><span class="sxs-lookup"><span data-stu-id="6ec88-126">This function has no associated import library or header file; you must call it using the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) functions.</span></span>

## <a name="requirements"></a><span data-ttu-id="6ec88-127">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6ec88-127">Requirements</span></span>



| <span data-ttu-id="6ec88-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="6ec88-128">Requirement</span></span> | <span data-ttu-id="6ec88-129">Valor</span><span class="sxs-lookup"><span data-stu-id="6ec88-129">Value</span></span> |
|----------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="6ec88-130">DLL</span><span class="sxs-lookup"><span data-stu-id="6ec88-130">DLL</span></span><br/> | <dl> <span data-ttu-id="6ec88-131"><dt>Msjter40.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6ec88-131"><dt>Msjter40.dll</dt></span></span> </dl> |



 

 
