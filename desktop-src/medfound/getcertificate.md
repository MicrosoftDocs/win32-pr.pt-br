---
description: Obtém um certificado para um driver de vídeo.
ms.assetid: eceaf151-1dae-4ff0-9139-7f1789f6c682
title: Função getcertificate
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetCertificate
api_type:
- DllExport
api_location:
- gdi32.dll
ms.openlocfilehash: 30cb17345177b552e51120afd00758a3f6886584
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105791537"
---
# <a name="getcertificate-function"></a><span data-ttu-id="e2259-103">Função getcertificate</span><span class="sxs-lookup"><span data-stu-id="e2259-103">GetCertificate function</span></span>

> [!IMPORTANT]
> <span data-ttu-id="e2259-104">Essa função é usada pelo [Gerenciador de proteção de saída](output-protection-manager.md) (OPM) para acessar a funcionalidade no driver de vídeo.</span><span class="sxs-lookup"><span data-stu-id="e2259-104">This function is used by [Output Protection Manager](output-protection-manager.md) (OPM) to access functionality in the display driver.</span></span> <span data-ttu-id="e2259-105">Os aplicativos não devem chamar essa função.</span><span class="sxs-lookup"><span data-stu-id="e2259-105">Applications should not call this function.</span></span>

 

<span data-ttu-id="e2259-106">Obtém um certificado para um driver de vídeo.</span><span class="sxs-lookup"><span data-stu-id="e2259-106">Gets a certificate for a display driver.</span></span>

## <a name="syntax"></a><span data-ttu-id="e2259-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="e2259-107">Syntax</span></span>


```C++
NTSTATUS WINAPI GetCertificate(
  _In_  PUNICODE_STRING          pstrDeviceName,
  _In_  DXGKMDT_CERTIFICATE_TYPE ctPVPCertificateType,
  _Out_ BYTE                     *pbCertificate,
  _Out_ ULONG                    ulCertificateLength
);
```



## <a name="parameters"></a><span data-ttu-id="e2259-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="e2259-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e2259-109">*pstrDeviceName* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="e2259-109">*pstrDeviceName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e2259-110">Um ponteiro para uma estrutura de [**\_ cadeia de caracteres Unicode**](/windows/win32/api/subauth/ns-subauth-unicode_string) que contém o nome do dispositivo de vídeo, conforme retornado pela função [**GetMonitorInfo**](/windows/win32/api/winuser/nf-winuser-getmonitorinfoa) .</span><span class="sxs-lookup"><span data-stu-id="e2259-110">A pointer to a [**UNICODE\_STRING**](/windows/win32/api/subauth/ns-subauth-unicode_string) structure that contains the name of the display device, as returned by the [**GetMonitorInfo**](/windows/win32/api/winuser/nf-winuser-getmonitorinfoa) function.</span></span>

</dd> <dt>

<span data-ttu-id="e2259-111">*ctPVPCertificateType* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="e2259-111">*ctPVPCertificateType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e2259-112">O tipo de certificado, especificado como um membro da enumeração **de \_ \_ tipo de certificado DXGKMDT** .</span><span class="sxs-lookup"><span data-stu-id="e2259-112">The type of certificate, specified as a member of the **DXGKMDT\_CERTIFICATE\_TYPE** enumeration.</span></span>

</dd> <dt>

<span data-ttu-id="e2259-113">*pbCertificate* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="e2259-113">*pbCertificate* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="e2259-114">Um ponteiro para um buffer que recebe o certificado.</span><span class="sxs-lookup"><span data-stu-id="e2259-114">A pointer to a buffer that receives the certificate.</span></span>

</dd> <dt>

<span data-ttu-id="e2259-115">*ulCertificateLength* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="e2259-115">*ulCertificateLength* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="e2259-116">O tamanho do buffer *pbCertificate* , em bytes.</span><span class="sxs-lookup"><span data-stu-id="e2259-116">The size of the *pbCertificate* buffer, in bytes.</span></span> <span data-ttu-id="e2259-117">Para obter o tamanho do certificado, chame [**Getcertificates**](getcertificatesize.md).</span><span class="sxs-lookup"><span data-stu-id="e2259-117">To get the size of the certificate, call [**GetCertificateSize**](getcertificatesize.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e2259-118">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="e2259-118">Return value</span></span>

<span data-ttu-id="e2259-119">Se o método for bem-sucedido, ele retornará o **status \_ êxito**.</span><span class="sxs-lookup"><span data-stu-id="e2259-119">If the method succeeds, it returns **STATUS\_SUCCESS**.</span></span> <span data-ttu-id="e2259-120">Caso contrário, ele retorna um código de erro **NTSTATUS** .</span><span class="sxs-lookup"><span data-stu-id="e2259-120">Otherwise, it returns an **NTSTATUS** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="e2259-121">Comentários</span><span class="sxs-lookup"><span data-stu-id="e2259-121">Remarks</span></span>

<span data-ttu-id="e2259-122">Os aplicativos devem chamar o método [**IOPMVideoOutput:: StartInitialization**](/windows/desktop/api/opmapi/nf-opmapi-iopmvideooutput-startinitialization) em vez desta função.</span><span class="sxs-lookup"><span data-stu-id="e2259-122">Applications should call the [**IOPMVideoOutput::StartInitialization**](/windows/desktop/api/opmapi/nf-opmapi-iopmvideooutput-startinitialization) method instead of this function.</span></span>

<span data-ttu-id="e2259-123">Esta função não tem biblioteca de importação associada.</span><span class="sxs-lookup"><span data-stu-id="e2259-123">This function has no associated import library.</span></span> <span data-ttu-id="e2259-124">Para chamar essa função, você deve usar as funções [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) e [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) para vincular dinamicamente a Gdi32.dll.</span><span class="sxs-lookup"><span data-stu-id="e2259-124">To call this function, you must use the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) functions to dynamically link to Gdi32.dll.</span></span>

## <a name="requirements"></a><span data-ttu-id="e2259-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e2259-125">Requirements</span></span>



| <span data-ttu-id="e2259-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="e2259-126">Requirement</span></span> | <span data-ttu-id="e2259-127">Valor</span><span class="sxs-lookup"><span data-stu-id="e2259-127">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="e2259-128">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="e2259-128">Minimum supported client</span></span><br/> | <span data-ttu-id="e2259-129">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="e2259-129">Windows Vista \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="e2259-130">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="e2259-130">Minimum supported server</span></span><br/> | <span data-ttu-id="e2259-131">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="e2259-131">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="e2259-132">DLL</span><span class="sxs-lookup"><span data-stu-id="e2259-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e2259-133"><dt>Gdi32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e2259-133"><dt>Gdi32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e2259-134">Confira também</span><span class="sxs-lookup"><span data-stu-id="e2259-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e2259-135">Funções OPM</span><span class="sxs-lookup"><span data-stu-id="e2259-135">OPM Functions</span></span>](opm-functions.md)
</dt> <dt>

[<span data-ttu-id="e2259-136">Gerenciador de proteção de saída</span><span class="sxs-lookup"><span data-stu-id="e2259-136">Output Protection Manager</span></span>](output-protection-manager.md)
</dt> </dl>

 

 
