---
title: Função TLSDisconnectFromServer
description: Fecha um identificador aberto para um servidor de licença Área de Trabalho Remota.
ms.assetid: b4b001ec-823b-4514-bbec-839a83a9a189
ms.tgt_platform: multiple
keywords:
- Função TLSDisconnectFromServer Serviços de Área de Trabalho Remota
topic_type:
- apiref
api_name:
- TLSDisconnectFromServer
api_location:
- Mstlsapi.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 265a6b04186bd640943cf2b348dda7afcf8f712a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105780096"
---
# <a name="tlsdisconnectfromserver-function"></a><span data-ttu-id="25fa2-104">Função TLSDisconnectFromServer</span><span class="sxs-lookup"><span data-stu-id="25fa2-104">TLSDisconnectFromServer function</span></span>

<span data-ttu-id="25fa2-105">Fecha um identificador aberto para um servidor de licença Área de Trabalho Remota.</span><span class="sxs-lookup"><span data-stu-id="25fa2-105">Closes an open handle to a Remote Desktop license server.</span></span>

> [!Note]  
> <span data-ttu-id="25fa2-106">Esta função não tem nenhum arquivo de cabeçalho ou biblioteca de importação associado.</span><span class="sxs-lookup"><span data-stu-id="25fa2-106">This function has no associated header file or import library.</span></span> <span data-ttu-id="25fa2-107">Para chamar essa função, você deve criar um arquivo de cabeçalho definido pelo usuário e usar as funções [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) e [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress) para vincular dinamicamente a Mstlsapi.dll.</span><span class="sxs-lookup"><span data-stu-id="25fa2-107">To call this function, you must create a user-defined header file and use the [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress) functions to dynamically link to Mstlsapi.dll.</span></span>

 

## <a name="syntax"></a><span data-ttu-id="25fa2-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="25fa2-108">Syntax</span></span>


```C++
void WINAPI TLSDisconnectFromServer(
  _In_ TLS_HANDLE hHandle
);
```



## <a name="parameters"></a><span data-ttu-id="25fa2-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="25fa2-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="25fa2-110">*hHandle* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="25fa2-110">*hHandle* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="25fa2-111">Identificador para um Área de Trabalho Remota servidor de licença que é aberto por uma chamada para a função [**TLSConnectToLsServer**](tlsconnecttolsserver.md) .</span><span class="sxs-lookup"><span data-stu-id="25fa2-111">Handle to a Remote Desktop license server that is opened by a call to the [**TLSConnectToLsServer**](tlsconnecttolsserver.md) function.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="25fa2-112">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="25fa2-112">Return value</span></span>

<span data-ttu-id="25fa2-113">Esse método não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="25fa2-113">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="25fa2-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="25fa2-114">Remarks</span></span>

<span data-ttu-id="25fa2-115">Chame a função **TLSDisconnectFromServer** como parte da rotina de limpeza do programa para fechar todos os identificadores do servidor que são abertos por chamadas para a função [**TLSConnectToLsServer**](tlsconnecttolsserver.md) .</span><span class="sxs-lookup"><span data-stu-id="25fa2-115">Call the **TLSDisconnectFromServer** function as part of your program's clean-up routine to close all the server handles that are opened by calls to the [**TLSConnectToLsServer**](tlsconnecttolsserver.md) function.</span></span>

## <a name="requirements"></a><span data-ttu-id="25fa2-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="25fa2-116">Requirements</span></span>



| <span data-ttu-id="25fa2-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="25fa2-117">Requirement</span></span> | <span data-ttu-id="25fa2-118">Valor</span><span class="sxs-lookup"><span data-stu-id="25fa2-118">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="25fa2-119">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="25fa2-119">Minimum supported client</span></span><br/> | <span data-ttu-id="25fa2-120">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="25fa2-120">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="25fa2-121">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="25fa2-121">Minimum supported server</span></span><br/> | <span data-ttu-id="25fa2-122">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="25fa2-122">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="25fa2-123">DLL</span><span class="sxs-lookup"><span data-stu-id="25fa2-123">DLL</span></span><br/>                      | <dl> <span data-ttu-id="25fa2-124"><dt>Mstlsapi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="25fa2-124"><dt>Mstlsapi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="25fa2-125">Confira também</span><span class="sxs-lookup"><span data-stu-id="25fa2-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="25fa2-126">**identificador de TLS \_**</span><span class="sxs-lookup"><span data-stu-id="25fa2-126">**TLS\_HANDLE**</span></span>](tls-handle.md)
</dt> <dt>

[<span data-ttu-id="25fa2-127">**TLSConnectToLsServer**</span><span class="sxs-lookup"><span data-stu-id="25fa2-127">**TLSConnectToLsServer**</span></span>](tlsconnecttolsserver.md)
</dt> </dl>

 

