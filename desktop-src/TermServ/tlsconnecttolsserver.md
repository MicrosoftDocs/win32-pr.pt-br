---
title: Função TLSConnectToLsServer
description: Abre um identificador para o servidor de licença de Área de Trabalho Remota especificado.
ms.assetid: 9e90a8e8-9319-42ee-b541-a1d028b6ed4d
ms.tgt_platform: multiple
keywords:
- Função TLSConnectToLsServer Serviços de Área de Trabalho Remota
topic_type:
- apiref
api_name:
- TLSConnectToLsServer
api_location:
- Mstlsapi.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fc7f36b519399f0a8c1627fad7c7768f36ece57f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104369719"
---
# <a name="tlsconnecttolsserver-function"></a><span data-ttu-id="51ab4-104">Função TLSConnectToLsServer</span><span class="sxs-lookup"><span data-stu-id="51ab4-104">TLSConnectToLsServer function</span></span>

<span data-ttu-id="51ab4-105">Abre um identificador para o servidor de licença de Área de Trabalho Remota especificado.</span><span class="sxs-lookup"><span data-stu-id="51ab4-105">Opens a handle to the specified Remote Desktop license server.</span></span>

> [!Note]  
> <span data-ttu-id="51ab4-106">Esta função não tem nenhum arquivo de cabeçalho ou biblioteca de importação associado.</span><span class="sxs-lookup"><span data-stu-id="51ab4-106">This function has no associated header file or import library.</span></span> <span data-ttu-id="51ab4-107">Para chamar essa função, você deve criar um arquivo de cabeçalho definido pelo usuário e usar as funções [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) e [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress) para vincular dinamicamente a Mstlsapi.dll.</span><span class="sxs-lookup"><span data-stu-id="51ab4-107">To call this function, you must create a user-defined header file and use the [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress) functions to dynamically link to Mstlsapi.dll.</span></span>

 

## <a name="syntax"></a><span data-ttu-id="51ab4-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="51ab4-108">Syntax</span></span>


```C++
TLS_HANDLE WINAPI TLSConnectToLsServer(
  _In_ LPTSTR pszLsServer
);
```



## <a name="parameters"></a><span data-ttu-id="51ab4-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="51ab4-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="51ab4-110">*pszLsServer* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="51ab4-110">*pszLsServer* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="51ab4-111">Ponteiro para uma cadeia de caracteres terminada em **nulo** que especifica o nome NetBIOS do servidor de licença área de trabalho remota.</span><span class="sxs-lookup"><span data-stu-id="51ab4-111">Pointer to a **null**-terminated string that specifies the NetBIOS name of the Remote Desktop license server.</span></span> <span data-ttu-id="51ab4-112">Se o valor desse parâmetro for **nulo**, o servidor especificado será o computador local.</span><span class="sxs-lookup"><span data-stu-id="51ab4-112">If the value of this parameter is **NULL**, the specified server is the local computer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="51ab4-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="51ab4-113">Return value</span></span>

<span data-ttu-id="51ab4-114">Se a função for realizada com sucesso, o valor de retorno será um identificador para o servidor especificado.</span><span class="sxs-lookup"><span data-stu-id="51ab4-114">If the function succeeds, the return value is a handle to the specified server.</span></span>

<span data-ttu-id="51ab4-115">Se a função falhar, o valor de retorno será **nulo**.</span><span class="sxs-lookup"><span data-stu-id="51ab4-115">If the function fails, the return value is **NULL**.</span></span> <span data-ttu-id="51ab4-116">Para obter informações de erro estendidas, chame a função [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) .</span><span class="sxs-lookup"><span data-stu-id="51ab4-116">To get extended error information, call the [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) function.</span></span>

## <a name="remarks"></a><span data-ttu-id="51ab4-117">Comentários</span><span class="sxs-lookup"><span data-stu-id="51ab4-117">Remarks</span></span>

<span data-ttu-id="51ab4-118">Quando você terminar de usar o identificador retornado pela função **TLSConnectToLsServer** , libere-o chamando a função [**TLSDisconnectFromServer**](tlsdisconnectfromserver.md) .</span><span class="sxs-lookup"><span data-stu-id="51ab4-118">When you have finished using the handle that is returned by the **TLSConnectToLsServer** function, release it by calling the [**TLSDisconnectFromServer**](tlsdisconnectfromserver.md) function.</span></span>

## <a name="requirements"></a><span data-ttu-id="51ab4-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="51ab4-119">Requirements</span></span>



| <span data-ttu-id="51ab4-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="51ab4-120">Requirement</span></span> | <span data-ttu-id="51ab4-121">Valor</span><span class="sxs-lookup"><span data-stu-id="51ab4-121">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="51ab4-122">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="51ab4-122">Minimum supported client</span></span><br/> | <span data-ttu-id="51ab4-123">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="51ab4-123">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="51ab4-124">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="51ab4-124">Minimum supported server</span></span><br/> | <span data-ttu-id="51ab4-125">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="51ab4-125">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="51ab4-126">DLL</span><span class="sxs-lookup"><span data-stu-id="51ab4-126">DLL</span></span><br/>                      | <dl> <span data-ttu-id="51ab4-127"><dt>Mstlsapi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="51ab4-127"><dt>Mstlsapi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="51ab4-128">Confira também</span><span class="sxs-lookup"><span data-stu-id="51ab4-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="51ab4-129">**identificador de TLS \_**</span><span class="sxs-lookup"><span data-stu-id="51ab4-129">**TLS\_HANDLE**</span></span>](tls-handle.md)
</dt> <dt>

[<span data-ttu-id="51ab4-130">**TLSDisconnectFromServer**</span><span class="sxs-lookup"><span data-stu-id="51ab4-130">**TLSDisconnectFromServer**</span></span>](tlsdisconnectfromserver.md)
</dt> </dl>

 

