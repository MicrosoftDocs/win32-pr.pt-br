---
description: Define ou recupera um valor de enumeração que especifica o nome do CAPICOM do EKU. Essa é a propriedade padrão.
ms.assetid: afce5553-ef18-4a7f-b1c8-fbe00d3277e0
title: 'Propriedade IEKU:: Name'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IEKU.Name
- IEKU.get_Name
- IEKU.put_Name
- EKU.Name
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: e0e28a8816d7e4c4f44e3cd1ec0dc479372d66d1
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105750093"
---
# <a name="iekuname-property"></a><span data-ttu-id="a30ef-104">Propriedade IEKU:: Name</span><span class="sxs-lookup"><span data-stu-id="a30ef-104">IEKU::Name property</span></span>

<span data-ttu-id="a30ef-105">\[O CAPICOM é um componente somente de 32 bits que está disponível para uso nos seguintes sistemas operacionais: Windows Server 2008, Windows Vista e Windows XP.</span><span class="sxs-lookup"><span data-stu-id="a30ef-105">\[CAPICOM is a 32-bit only component that is available for use in the following operating systems: Windows Server 2008, Windows Vista, and Windows XP.</span></span> <span data-ttu-id="a30ef-106">Em vez disso, use a [**classe X509EnhancedKeyUsageExtension**](/dotnet/api/system.security.cryptography.x509certificates.x509enhancedkeyusageextension?view=netcore-3.1) no namespace [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) .\]</span><span class="sxs-lookup"><span data-stu-id="a30ef-106">Instead, use the [**X509EnhancedKeyUsageExtension Class**](/dotnet/api/system.security.cryptography.x509certificates.x509enhancedkeyusageextension?view=netcore-3.1) in the [**System.Security.Cryptography.X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) namespace.\]</span></span>

<span data-ttu-id="a30ef-107">A propriedade **Name** define ou recupera um valor de enumeração que especifica o nome do CAPICOM do EKU.</span><span class="sxs-lookup"><span data-stu-id="a30ef-107">The **Name** property sets or retrieves an enumeration value that specifies the CAPICOM name of the EKU.</span></span> <span data-ttu-id="a30ef-108">Essa é a propriedade padrão.</span><span class="sxs-lookup"><span data-stu-id="a30ef-108">This is the default property.</span></span>

<span data-ttu-id="a30ef-109">Esta propriedade é de leitura/gravação.</span><span class="sxs-lookup"><span data-stu-id="a30ef-109">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="a30ef-110">Syntax</span><span class="sxs-lookup"><span data-stu-id="a30ef-110">Syntax</span></span>


```VB
EKU.Name As CAPICOM_EKU
```



## <a name="property-value"></a><span data-ttu-id="a30ef-111">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="a30ef-111">Property value</span></span>

<span data-ttu-id="a30ef-112">Um valor da enumeração [**\_ EKU de CAPICOM**](capicom-eku.md) que especifica o nome do CAPICOM do EKU.</span><span class="sxs-lookup"><span data-stu-id="a30ef-112">A value of the [**CAPICOM\_EKU**](capicom-eku.md) enumeration that specifies the CAPICOM name of the EKU.</span></span> <span data-ttu-id="a30ef-113">A tabela a seguir mostra os valores possíveis.</span><span class="sxs-lookup"><span data-stu-id="a30ef-113">The following table shows the possible values.</span></span>



| <span data-ttu-id="a30ef-114">Valor</span><span class="sxs-lookup"><span data-stu-id="a30ef-114">Value</span></span>                                                                                                                                                                                                                           | <span data-ttu-id="a30ef-115">Significado</span><span class="sxs-lookup"><span data-stu-id="a30ef-115">Meaning</span></span>                                                                                                                                                     |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="CAPICOM_EKU_OTHER"></span><span id="capicom_eku_other"></span><dl> <span data-ttu-id="a30ef-116"><dt>**\_outro EKU de CApicom \_**</dt></span><span class="sxs-lookup"><span data-stu-id="a30ef-116"><dt>**CAPICOM\_EKU\_OTHER**</dt></span></span> </dl>                                                      | <span data-ttu-id="a30ef-117">O certificado tem usos definidos na política local.</span><span class="sxs-lookup"><span data-stu-id="a30ef-117">Certificate has uses defined in local policy.</span></span> <span data-ttu-id="a30ef-118">Isso será usado se o EKU necessário não for predefinido e o valor de OID precisar ser definido pelo aplicativo.</span><span class="sxs-lookup"><span data-stu-id="a30ef-118">This is used if the EKU needed is not predefined and the OID value must be set by the application.</span></span><br/> |
| <span id="CAPICOM_EKU_SERVER_AUTH"></span><span id="capicom_eku_server_auth"></span><dl> <span data-ttu-id="a30ef-119"><dt>**\_autenticação de \_ servidor de EKU capicor \_**</dt></span><span class="sxs-lookup"><span data-stu-id="a30ef-119"><dt>**CAPICOM\_EKU\_SERVER\_AUTH**</dt></span></span> </dl>                                   | <span data-ttu-id="a30ef-120">O certificado pode ser usado para autenticar um servidor.</span><span class="sxs-lookup"><span data-stu-id="a30ef-120">Certificate can be used to authenticate a server.</span></span><br/>                                                                                                |
| <span id="CAPICOM_EKU_CLIENT_AUTH"></span><span id="capicom_eku_client_auth"></span><dl> <span data-ttu-id="a30ef-121"><dt>**\_autenticação de \_ cliente de EKU capicor \_**</dt></span><span class="sxs-lookup"><span data-stu-id="a30ef-121"><dt>**CAPICOM\_EKU\_CLIENT\_AUTH**</dt></span></span> </dl>                                   | <span data-ttu-id="a30ef-122">O certificado pode ser usado para autenticar um cliente.</span><span class="sxs-lookup"><span data-stu-id="a30ef-122">Certificate can be used to authenticate a client.</span></span><br/>                                                                                                |
| <span id="CAPICOM_EKU_CODE_SIGNING"></span><span id="capicom_eku_code_signing"></span><dl> <span data-ttu-id="a30ef-123"><dt>**\_assinatura de \_ código de EKU CAPICOM \_**</dt></span><span class="sxs-lookup"><span data-stu-id="a30ef-123"><dt>**CAPICOM\_EKU\_CODE\_SIGNING**</dt></span></span> </dl>                                | <span data-ttu-id="a30ef-124">O certificado pode ser usado para criar uma assinatura digital.</span><span class="sxs-lookup"><span data-stu-id="a30ef-124">Certificate can be used to create a digital signature.</span></span><br/>                                                                                           |
| <span id="CAPICOM_EKU_EMAIL_PROTECTION"></span><span id="capicom_eku_email_protection"></span><dl> <span data-ttu-id="a30ef-125"><dt>**\_proteção de \_ email de EKU CAPICOM \_**</dt></span><span class="sxs-lookup"><span data-stu-id="a30ef-125"><dt>**CAPICOM\_EKU\_EMAIL\_PROTECTION**</dt></span></span> </dl>                    | <span data-ttu-id="a30ef-126">O certificado pode ser usado para proteção de email.</span><span class="sxs-lookup"><span data-stu-id="a30ef-126">Certificate can be used for email protection.</span></span><br/>                                                                                                    |
| <span id="CAPICOM_EKU_SMARTCARD_LOGON"></span><span id="capicom_eku_smartcard_logon"></span><dl> <span data-ttu-id="a30ef-127"><dt>**\_logon de \_ cartão inteligente \_ capicor EKU**</dt></span><span class="sxs-lookup"><span data-stu-id="a30ef-127"><dt>**CAPICOM\_EKU\_SMARTCARD\_LOGON**</dt></span></span> </dl>                       | <span data-ttu-id="a30ef-128">O certificado pode ser usado para logon de cartão inteligente.</span><span class="sxs-lookup"><span data-stu-id="a30ef-128">Certificate can be used for smart card logon.</span></span> <span data-ttu-id="a30ef-129">Introduzido no CAPICOM 2,0.</span><span class="sxs-lookup"><span data-stu-id="a30ef-129">Introduced in CAPICOM 2.0.</span></span><br/>                                                                         |
| <span id="CAPICOM_EKU_ENCRYPTING_FILE_SYSTEM"></span><span id="capicom_eku_encrypting_file_system"></span><dl> <span data-ttu-id="a30ef-130"><dt>**\_sistema de \_ arquivos com criptografia EKU \_ de CAPICOM \_**</dt></span><span class="sxs-lookup"><span data-stu-id="a30ef-130"><dt>**CAPICOM\_EKU\_ENCRYPTING\_FILE\_SYSTEM**</dt></span></span> </dl> | <span data-ttu-id="a30ef-131">O certificado pode ser usado para o EFS.</span><span class="sxs-lookup"><span data-stu-id="a30ef-131">Certificate can be used for EFS.</span></span> <span data-ttu-id="a30ef-132">Introduzido no CAPICOM 2,0.</span><span class="sxs-lookup"><span data-stu-id="a30ef-132">Introduced in CAPICOM 2.0.</span></span><br/>                                                                                      |



 

## <a name="remarks"></a><span data-ttu-id="a30ef-133">Comentários</span><span class="sxs-lookup"><span data-stu-id="a30ef-133">Remarks</span></span>

<span data-ttu-id="a30ef-134">Quando o valor dessa propriedade é redefinido, direta ou indiretamente, o [*estado*](../secgloss/s-gly.md) inteiro do objeto é redefinido.</span><span class="sxs-lookup"><span data-stu-id="a30ef-134">When the value of this property is reset, directly or indirectly, the whole [*state*](../secgloss/s-gly.md) of the object is reset.</span></span>

## <a name="requirements"></a><span data-ttu-id="a30ef-135">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a30ef-135">Requirements</span></span>



| <span data-ttu-id="a30ef-136">Requisito</span><span class="sxs-lookup"><span data-stu-id="a30ef-136">Requirement</span></span> | <span data-ttu-id="a30ef-137">Valor</span><span class="sxs-lookup"><span data-stu-id="a30ef-137">Value</span></span> |
|----------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="a30ef-138">Fim do suporte do cliente</span><span class="sxs-lookup"><span data-stu-id="a30ef-138">End of client support</span></span><br/> | <span data-ttu-id="a30ef-139">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="a30ef-139">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="a30ef-140">Fim do suporte do servidor</span><span class="sxs-lookup"><span data-stu-id="a30ef-140">End of server support</span></span><br/> | <span data-ttu-id="a30ef-141">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="a30ef-141">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="a30ef-142">Redistribuível</span><span class="sxs-lookup"><span data-stu-id="a30ef-142">Redistributable</span></span><br/>       | <span data-ttu-id="a30ef-143">CAPICOM 2,0 ou posterior no Windows Server 2003 e no Windows XP</span><span class="sxs-lookup"><span data-stu-id="a30ef-143">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="a30ef-144">DLL</span><span class="sxs-lookup"><span data-stu-id="a30ef-144">DLL</span></span><br/>                   | <dl> <span data-ttu-id="a30ef-145"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a30ef-145"><dt>Capicom.dll</dt></span></span> </dl> |



 

 
