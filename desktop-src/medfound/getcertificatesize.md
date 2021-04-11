---
description: Obtém o tamanho de um certificado para um driver de vídeo.
ms.assetid: fd52e939-127a-4493-8406-31f7767921cd
title: Função getcertificate
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetCertificateSize
api_type:
- DllExport
api_location:
- gdi32.dll
ms.openlocfilehash: bcd1f49ce65978c6a89c89cee1fda38e41434065
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104296140"
---
# <a name="getcertificatesize-function"></a><span data-ttu-id="b6197-103">Função getcertificate</span><span class="sxs-lookup"><span data-stu-id="b6197-103">GetCertificateSize function</span></span>

> [!IMPORTANT]
> <span data-ttu-id="b6197-104">Essa função é usada pelo [Gerenciador de proteção de saída](output-protection-manager.md) (OPM) para acessar a funcionalidade no driver de vídeo.</span><span class="sxs-lookup"><span data-stu-id="b6197-104">This function is used by [Output Protection Manager](output-protection-manager.md) (OPM) to access functionality in the display driver.</span></span> <span data-ttu-id="b6197-105">Os aplicativos não devem chamar essa função.</span><span class="sxs-lookup"><span data-stu-id="b6197-105">Applications should not call this function.</span></span>

 

<span data-ttu-id="b6197-106">Obtém o tamanho de um certificado para um driver de vídeo.</span><span class="sxs-lookup"><span data-stu-id="b6197-106">Gets the size of a certificate for a display driver.</span></span>

## <a name="syntax"></a><span data-ttu-id="b6197-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="b6197-107">Syntax</span></span>


```C++
NTSTATUS WINAPI GetCertificateSize(
  _In_  PUNICODE_STRING          pstrDeviceName,
  _In_  DXGKMDT_CERTIFICATE_TYPE ctPVPCertificateType,
  _Out_ ULONG                    *pulCertificateLength
);
```



## <a name="parameters"></a><span data-ttu-id="b6197-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="b6197-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b6197-109">*pstrDeviceName* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="b6197-109">*pstrDeviceName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b6197-110">Um ponteiro para uma estrutura de [**\_ cadeia de caracteres Unicode**](/windows/win32/api/subauth/ns-subauth-unicode_string) que contém o nome do dispositivo de vídeo, conforme retornado pela função [**GetMonitorInfo**](/windows/win32/api/winuser/nf-winuser-getmonitorinfoa) .</span><span class="sxs-lookup"><span data-stu-id="b6197-110">A pointer to a [**UNICODE\_STRING**](/windows/win32/api/subauth/ns-subauth-unicode_string) structure that contains the name of the display device, as returned by the [**GetMonitorInfo**](/windows/win32/api/winuser/nf-winuser-getmonitorinfoa) function.</span></span>

</dd> <dt>

<span data-ttu-id="b6197-111">*ctPVPCertificateType* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="b6197-111">*ctPVPCertificateType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b6197-112">O tipo de certificado, especificado como um membro da enumeração **de \_ \_ tipo de certificado DXGKMDT** .</span><span class="sxs-lookup"><span data-stu-id="b6197-112">The type of certificate, specified as a member of the **DXGKMDT\_CERTIFICATE\_TYPE** enumeration.</span></span>

</dd> <dt>

<span data-ttu-id="b6197-113">*pulCertificateLength* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="b6197-113">*pulCertificateLength* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="b6197-114">Recebe o tamanho do certificado, em bytes.</span><span class="sxs-lookup"><span data-stu-id="b6197-114">Receives the size of the certificate, in bytes.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b6197-115">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="b6197-115">Return value</span></span>

<span data-ttu-id="b6197-116">Se o método for bem-sucedido, ele retornará o **status \_ êxito**.</span><span class="sxs-lookup"><span data-stu-id="b6197-116">If the method succeeds, it returns **STATUS\_SUCCESS**.</span></span> <span data-ttu-id="b6197-117">Caso contrário, ele retorna um código de erro **NTSTATUS** .</span><span class="sxs-lookup"><span data-stu-id="b6197-117">Otherwise, it returns an **NTSTATUS** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="b6197-118">Comentários</span><span class="sxs-lookup"><span data-stu-id="b6197-118">Remarks</span></span>

<span data-ttu-id="b6197-119">Os aplicativos devem chamar o método [**IOPMVideoOutput:: StartInitialization**](/windows/desktop/api/opmapi/nf-opmapi-iopmvideooutput-startinitialization) em vez desta função.</span><span class="sxs-lookup"><span data-stu-id="b6197-119">Applications should call the [**IOPMVideoOutput::StartInitialization**](/windows/desktop/api/opmapi/nf-opmapi-iopmvideooutput-startinitialization) method instead of this function.</span></span>

<span data-ttu-id="b6197-120">Esta função não tem biblioteca de importação associada.</span><span class="sxs-lookup"><span data-stu-id="b6197-120">This function has no associated import library.</span></span> <span data-ttu-id="b6197-121">Para chamar essa função, você deve usar as funções [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) e [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) para vincular dinamicamente a Gdi32.dll.</span><span class="sxs-lookup"><span data-stu-id="b6197-121">To call this function, you must use the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) functions to dynamically link to Gdi32.dll.</span></span>

## <a name="requirements"></a><span data-ttu-id="b6197-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b6197-122">Requirements</span></span>



| <span data-ttu-id="b6197-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="b6197-123">Requirement</span></span> | <span data-ttu-id="b6197-124">Valor</span><span class="sxs-lookup"><span data-stu-id="b6197-124">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="b6197-125">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="b6197-125">Minimum supported client</span></span><br/> | <span data-ttu-id="b6197-126">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="b6197-126">Windows Vista \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="b6197-127">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="b6197-127">Minimum supported server</span></span><br/> | <span data-ttu-id="b6197-128">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="b6197-128">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="b6197-129">DLL</span><span class="sxs-lookup"><span data-stu-id="b6197-129">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b6197-130"><dt>Gdi32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b6197-130"><dt>Gdi32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b6197-131">Confira também</span><span class="sxs-lookup"><span data-stu-id="b6197-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b6197-132">Funções OPM</span><span class="sxs-lookup"><span data-stu-id="b6197-132">OPM Functions</span></span>](opm-functions.md)
</dt> <dt>

[<span data-ttu-id="b6197-133">Gerenciador de proteção de saída</span><span class="sxs-lookup"><span data-stu-id="b6197-133">Output Protection Manager</span></span>](output-protection-manager.md)
</dt> </dl>

 

 
