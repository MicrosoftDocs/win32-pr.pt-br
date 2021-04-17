---
description: Baixa a assinatura do arquivo. cab, verifica as permissões associadas aos pacotes e as executa com base na autenticação.
ms.assetid: b86a8f39-73a1-4e17-ac83-9ed095de4922
title: Função DownloadJavaEX
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DownloadJavaEX
api_type:
- DllExport
api_location:
- Javacypt.dll
ms.openlocfilehash: 31371e91599d604db591ee3e921b42bc809aae21
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105811132"
---
# <a name="downloadjavaex-function"></a><span data-ttu-id="453d3-103">Função DownloadJavaEX</span><span class="sxs-lookup"><span data-stu-id="453d3-103">DownloadJavaEX function</span></span>

<span data-ttu-id="453d3-104">Baixa a assinatura do arquivo. cab, verifica as permissões associadas aos pacotes e as executa com base na autenticação.</span><span class="sxs-lookup"><span data-stu-id="453d3-104">Downloads the .cab file signature, verifies the permissions associated with the packages, and executes them based on authentication.</span></span>

## <a name="syntax"></a><span data-ttu-id="453d3-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="453d3-105">Syntax</span></span>


```C++
HRESULT WINAPI DownloadJavaEX(
  _In_ PALLOCATOR               Reserved,
  _In_ PCRYPT_PROVIDER_DATA     pProviderData,
  _In_ PJAVA_POLICY_PROVIDER    pJava,
  _In_ CRYPT_PROVIDER_FUNCTIONS *pFunctions,
  _In_ BOOL                     fCertificate,
  _In_ PJAVA_TRUST              pTrust
);
```



## <a name="parameters"></a><span data-ttu-id="453d3-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="453d3-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="453d3-107">*Reservado* \[ para no\]</span><span class="sxs-lookup"><span data-stu-id="453d3-107">*Reserved* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="453d3-108">Esse parâmetro é reservado.</span><span class="sxs-lookup"><span data-stu-id="453d3-108">This parameter is reserved.</span></span>

</dd> <dt>

<span data-ttu-id="453d3-109">*pProviderData* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="453d3-109">*pProviderData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="453d3-110">Uma estrutura de [**\_ \_ dados de provedor cript**](/windows/win32/api/wintrust/ns-wintrust-crypt_provider_data) que contém dados de certificado, como permissões de arquivo e de zona.</span><span class="sxs-lookup"><span data-stu-id="453d3-110">A [**CRYPT\_PROVIDER\_DATA**](/windows/win32/api/wintrust/ns-wintrust-crypt_provider_data) structure that contains certificate data such as file and zone permissions.</span></span>

</dd> <dt>

<span data-ttu-id="453d3-111">*pJava* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="453d3-111">*pJava* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="453d3-112">Uma estrutura de [**\_ \_ provedor de política Java**](/previous-versions//bb432350(v=vs.85)) que contém dados relacionados ao provedor de política.</span><span class="sxs-lookup"><span data-stu-id="453d3-112">A [**JAVA\_POLICY\_PROVIDER**](/previous-versions//bb432350(v=vs.85)) structure that contains data related to the policy provider.</span></span>

</dd> <dt>

<span data-ttu-id="453d3-113">*pFunctions* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="453d3-113">*pFunctions* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="453d3-114">Uma estrutura de [**\_ \_ funções de provedor criptografada**](/windows/win32/api/wintrust/ns-wintrust-crypt_provider_functions) que contém uma lista de métodos para verificar objetos de certificado, assinaturas e políticas finais.</span><span class="sxs-lookup"><span data-stu-id="453d3-114">A [**CRYPT\_PROVIDER\_FUNCTIONS**](/windows/win32/api/wintrust/ns-wintrust-crypt_provider_functions) structure that contains a list of methods to verify certificate objects, signatures, and final policies.</span></span>

</dd> <dt>

<span data-ttu-id="453d3-115">*fCertificate* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="453d3-115">*fCertificate* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="453d3-116">Se um certificado estiver presente, esse parâmetro será **true**.</span><span class="sxs-lookup"><span data-stu-id="453d3-116">If a certificate is present, this parameter is **TRUE**.</span></span> <span data-ttu-id="453d3-117">Caso contrário, será **false**.</span><span class="sxs-lookup"><span data-stu-id="453d3-117">Otherwise, it is **FALSE**.</span></span>

</dd> <dt>

<span data-ttu-id="453d3-118">*pTrust* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="453d3-118">*pTrust* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="453d3-119">Uma estrutura de [**\_ confiança do Java**](/windows/desktop/api/Capi/ns-capi-java_trust) que contém informações de confiança, como permissão codificada, assinatura do codificador e código de política de retorno autêntico.</span><span class="sxs-lookup"><span data-stu-id="453d3-119">A [**JAVA\_TRUST**](/windows/desktop/api/Capi/ns-capi-java_trust) structure that contains trust information such as encoded permission, encoder signature, and authentic return policy code.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="453d3-120">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="453d3-120">Return value</span></span>

<span data-ttu-id="453d3-121">Se a função for bem sucedido, o valor de retorno será **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="453d3-121">If the function succeeds, the return value is **S\_OK**.</span></span> <span data-ttu-id="453d3-122">Caso contrário, o valor de retorno será um código de erro.</span><span class="sxs-lookup"><span data-stu-id="453d3-122">Otherwise, the return value is an error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="453d3-123">Comentários</span><span class="sxs-lookup"><span data-stu-id="453d3-123">Remarks</span></span>

<span data-ttu-id="453d3-124">Esta função não tem biblioteca de importação ou arquivo de cabeçalho associado; Você deve chamá-lo usando as funções [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) e [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) .</span><span class="sxs-lookup"><span data-stu-id="453d3-124">This function has no associated import library or header file; you must call it using the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) functions.</span></span>

## <a name="requirements"></a><span data-ttu-id="453d3-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="453d3-125">Requirements</span></span>



| <span data-ttu-id="453d3-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="453d3-126">Requirement</span></span> | <span data-ttu-id="453d3-127">Valor</span><span class="sxs-lookup"><span data-stu-id="453d3-127">Value</span></span> |
|----------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="453d3-128">DLL</span><span class="sxs-lookup"><span data-stu-id="453d3-128">DLL</span></span><br/> | <dl> <span data-ttu-id="453d3-129"><dt>Javacypt.dll</dt></span><span class="sxs-lookup"><span data-stu-id="453d3-129"><dt>Javacypt.dll</dt></span></span> </dl> |



 

 
