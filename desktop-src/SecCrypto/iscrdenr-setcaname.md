---
description: Especifica o nome da autoridade de certificação (CA).
ms.assetid: 224c2a51-8a25-4b66-b86b-c87531475145
title: 'Método ISCrdEnr:: setCAName'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCrdEnr.setCAName
- SCrdEnr.setCAName
api_type:
- COM
api_location:
- Scrdenrl.dll
ms.openlocfilehash: 46dcd9294337c088b9e1b0ab68bddefe4308ed27
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105756856"
---
# <a name="iscrdenrsetcaname-method"></a><span data-ttu-id="e0f50-103">Método ISCrdEnr:: setCAName</span><span class="sxs-lookup"><span data-stu-id="e0f50-103">ISCrdEnr::setCAName method</span></span>

<span data-ttu-id="e0f50-104">O método **setCAName** especifica o nome da [*autoridade de certificação*](../secgloss/c-gly.md) (CA).</span><span class="sxs-lookup"><span data-stu-id="e0f50-104">The **setCAName** method specifies the name of the [*certification authority*](../secgloss/c-gly.md) (CA).</span></span>

## <a name="syntax"></a><span data-ttu-id="e0f50-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="e0f50-105">Syntax</span></span>


```C++
HRESULT setCAName(
  [in] DWORD dwFlags,
  [in] BSTR bstrCertTemplateName,
  [in] BSTR bstrCAName
);
```


```VB

SCrdEnr.setCAName( _
  ByVal dwFlags, _
  ByVal bstrCertTemplateName, _
  ByVal bstrCAName _
)
```





## <a name="parameters"></a><span data-ttu-id="e0f50-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="e0f50-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e0f50-107">*dwFlags* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="e0f50-107">*dwFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e0f50-108">Valor que especifica se o nome refere-se ao nome da autoridade de certificação ou ao nome da máquina da autoridade de certificação.</span><span class="sxs-lookup"><span data-stu-id="e0f50-108">Value that specifies whether the name refers to the CA name or the CA's machine name.</span></span> <span data-ttu-id="e0f50-109">Se esse valor for SCARTAR \_ , registre o \_ \_ nome da máquina CA \_ (definido como 0x01), o nome se referirá ao nome da máquina da autoridade de certificação.</span><span class="sxs-lookup"><span data-stu-id="e0f50-109">If this value is SCARD\_ENROLL\_CA\_MACHINE\_NAME (defined as 0x01), the name refers to the CA's machine name.</span></span> <span data-ttu-id="e0f50-110">Caso contrário, o nome se refere ao nome da autoridade de certificação.</span><span class="sxs-lookup"><span data-stu-id="e0f50-110">Otherwise, the name refers to the CA name.</span></span>

</dd> <dt>

<span data-ttu-id="e0f50-111">*bstrCertTemplateName* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="e0f50-111">*bstrCertTemplateName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e0f50-112">Nome do modelo de certificado.</span><span class="sxs-lookup"><span data-stu-id="e0f50-112">Name of the certificate template.</span></span>

</dd> <dt>

<span data-ttu-id="e0f50-113">*bstrCAName* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="e0f50-113">*bstrCAName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e0f50-114">Nome da autoridade de certificação a ser usado com o modelo de certificado especificado por *bstrCertTemplateName*.</span><span class="sxs-lookup"><span data-stu-id="e0f50-114">CA name to be used with the certificate template specified by *bstrCertTemplateName*.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e0f50-115">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="e0f50-115">Return value</span></span>

### <a name="vb"></a><span data-ttu-id="e0f50-116">VB</span><span class="sxs-lookup"><span data-stu-id="e0f50-116">VB</span></span>

<span data-ttu-id="e0f50-117">O valor de retorno é um **HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="e0f50-117">The return value is an **HRESULT**.</span></span> <span data-ttu-id="e0f50-118">Um valor de S \_ OK indica que a chamada foi bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="e0f50-118">A value of S\_OK indicates that the call was successful.</span></span>

## <a name="remarks"></a><span data-ttu-id="e0f50-119">Comentários</span><span class="sxs-lookup"><span data-stu-id="e0f50-119">Remarks</span></span>

<span data-ttu-id="e0f50-120">Use esse método para especificar uma autoridade de certificação para um modelo de certificado.</span><span class="sxs-lookup"><span data-stu-id="e0f50-120">Use this method to specify a CA for a certificate template.</span></span>

## <a name="requirements"></a><span data-ttu-id="e0f50-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e0f50-121">Requirements</span></span>



| <span data-ttu-id="e0f50-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="e0f50-122">Requirement</span></span> | <span data-ttu-id="e0f50-123">Valor</span><span class="sxs-lookup"><span data-stu-id="e0f50-123">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="e0f50-124">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="e0f50-124">Minimum supported client</span></span><br/> | <span data-ttu-id="e0f50-125">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="e0f50-125">None supported</span></span><br/>                                                               |
| <span data-ttu-id="e0f50-126">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="e0f50-126">Minimum supported server</span></span><br/> | <span data-ttu-id="e0f50-127">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="e0f50-127">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="e0f50-128">DLL</span><span class="sxs-lookup"><span data-stu-id="e0f50-128">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e0f50-129"><dt>Scrdenrl.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e0f50-129"><dt>Scrdenrl.dll</dt></span></span> </dl> |
| <span data-ttu-id="e0f50-130">IID</span><span class="sxs-lookup"><span data-stu-id="e0f50-130">IID</span></span><br/>                      | <span data-ttu-id="e0f50-131">IID \_ ISCrdEnr é definido como 753988a1-1357-436d-9cf5-f089bdd67d64</span><span class="sxs-lookup"><span data-stu-id="e0f50-131">IID\_ISCrdEnr is defined as 753988a1-1357-436d-9cf5-f089bdd67d64</span></span><br/>             |



## <a name="see-also"></a><span data-ttu-id="e0f50-132">Confira também</span><span class="sxs-lookup"><span data-stu-id="e0f50-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e0f50-133">**ISCrdEnr**</span><span class="sxs-lookup"><span data-stu-id="e0f50-133">**ISCrdEnr**</span></span>](iscrdenr.md)
</dt> <dt>

[<span data-ttu-id="e0f50-134">**ISCrdEnr::enumCAName**</span><span class="sxs-lookup"><span data-stu-id="e0f50-134">**ISCrdEnr::enumCAName**</span></span>](iscrdenr-enumcaname.md)
</dt> <dt>

[<span data-ttu-id="e0f50-135">**ISCrdEnr::getCAName**</span><span class="sxs-lookup"><span data-stu-id="e0f50-135">**ISCrdEnr::getCAName**</span></span>](iscrdenr-getcaname.md)
</dt> </dl>

 

 
