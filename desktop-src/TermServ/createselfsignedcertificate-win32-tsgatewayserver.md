---
title: Método CreateSelfSignedCertificate da classe Win32_TSGatewayServer
description: Cria um certificado autoassinado e retorna o hash de certificado como um \ 0034; out \ 0034; meter.
ms.assetid: 2a5b8dee-50b8-44b7-9e29-25aff1c40f5d
ms.tgt_platform: multiple
keywords:
- Serviços de Área de Trabalho Remota do método CreateSelfSignedCertificate
- Método CreateSelfSignedCertificate Serviços de Área de Trabalho Remota, classe Win32_TSGatewayServer
- Classe Win32_TSGatewayServer Serviços de Área de Trabalho Remota, método CreateSelfSignedCertificate
topic_type:
- apiref
api_name:
- Win32_TSGatewayServer.CreateSelfSignedCertificate
api_location:
- AagWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4258566856a5fbc277053b65afe972751855d831
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104454787"
---
# <a name="createselfsignedcertificate-method-of-the-win32_tsgatewayserver-class"></a><span data-ttu-id="823aa-106">Método CreateSelfSignedCertificate da classe Win32 \_ TSGatewayServer</span><span class="sxs-lookup"><span data-stu-id="823aa-106">CreateSelfSignedCertificate method of the Win32\_TSGatewayServer class</span></span>

<span data-ttu-id="823aa-107">Cria um certificado autoassinado e retorna o hash de certificado como um parâmetro "out".</span><span class="sxs-lookup"><span data-stu-id="823aa-107">Creates a self-signed certificate and returns the certificate hash as an "out" parameter.</span></span> <span data-ttu-id="823aa-108">Além disso, o adiciona o texto \_ " \_ \_ certificado autoassinado de Gateway TS \_ " à propriedade de contexto de certificado para que o certificado seja reconhecido como um certificado de gateway de área de trabalho remota (gateway de área de trabalho remota).</span><span class="sxs-lookup"><span data-stu-id="823aa-108">Also, adds the text "TS\_GATEWAY\_SELF\_SIGNED\_CERTIFICATE" to the certificate context property so that the certificate is recognized as a Remote Desktop Gateway (RD Gateway) certificate.</span></span> <span data-ttu-id="823aa-109">Esse método usa um contêiner de chave específico do gateway de área de trabalho remota para criar o certificado.</span><span class="sxs-lookup"><span data-stu-id="823aa-109">This method uses an RD Gateway-specific key container to create the certificate.</span></span>

## <a name="syntax"></a><span data-ttu-id="823aa-110">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="823aa-110">Syntax</span></span>


```mof
uint32 CreateSelfSignedCertificate(
  [in]  string SubjectName,
  [out] uint8  CertHash[]
);
```



## <a name="parameters"></a><span data-ttu-id="823aa-111">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="823aa-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="823aa-112">*SubjectName* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="823aa-112">*SubjectName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="823aa-113">Nome da entidade do certificado autoassinado.</span><span class="sxs-lookup"><span data-stu-id="823aa-113">Subject name of the self-signed certificate.</span></span>

</dd> <dt>

<span data-ttu-id="823aa-114">*CertHash* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="823aa-114">*CertHash* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="823aa-115">O hash do certificado.</span><span class="sxs-lookup"><span data-stu-id="823aa-115">The certificate hash.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="823aa-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="823aa-116">Remarks</span></span>

<span data-ttu-id="823aa-117">Você deve ser um membro do grupo Administradores para chamar esse método.</span><span class="sxs-lookup"><span data-stu-id="823aa-117">You must be a member of the Administrators group to call this method.</span></span>

<span data-ttu-id="823aa-118">Os arquivos de formato MOF (MOF) contêm as definições de classes de Instrumentação de Gerenciamento do Windows (WMI).</span><span class="sxs-lookup"><span data-stu-id="823aa-118">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="823aa-119">Os arquivos MOF não são instalados como parte do SDK (Software Development Kit) do Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="823aa-119">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="823aa-120">Eles são instalados no servidor quando você adiciona a função associada usando o Gerenciador do Servidor.</span><span class="sxs-lookup"><span data-stu-id="823aa-120">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="823aa-121">Para obter mais informações sobre arquivos MOF, consulte [formato MOF (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="823aa-121">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="823aa-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="823aa-122">Requirements</span></span>



| <span data-ttu-id="823aa-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="823aa-123">Requirement</span></span> | <span data-ttu-id="823aa-124">Valor</span><span class="sxs-lookup"><span data-stu-id="823aa-124">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="823aa-125">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="823aa-125">Minimum supported client</span></span><br/> | <span data-ttu-id="823aa-126">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="823aa-126">None supported</span></span><br/>                                                                |
| <span data-ttu-id="823aa-127">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="823aa-127">Minimum supported server</span></span><br/> | <span data-ttu-id="823aa-128">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="823aa-128">Windows Server 2008</span></span><br/>                                                           |
| <span data-ttu-id="823aa-129">Namespace</span><span class="sxs-lookup"><span data-stu-id="823aa-129">Namespace</span></span><br/>                | <span data-ttu-id="823aa-130">\\TerminalServices da CIMv2 raiz \\</span><span class="sxs-lookup"><span data-stu-id="823aa-130">Root\\CIMv2\\TerminalServices</span></span><br/>                                                 |
| <span data-ttu-id="823aa-131">MOF</span><span class="sxs-lookup"><span data-stu-id="823aa-131">MOF</span></span><br/>                      | <dl> <span data-ttu-id="823aa-132"><dt>TS. mof</dt></span><span class="sxs-lookup"><span data-stu-id="823aa-132"><dt>TSGateway.mof</dt></span></span> </dl> |
| <span data-ttu-id="823aa-133">DLL</span><span class="sxs-lookup"><span data-stu-id="823aa-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="823aa-134"><dt>AagWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="823aa-134"><dt>AagWmi.dll</dt></span></span> </dl>    |



## <a name="see-also"></a><span data-ttu-id="823aa-135">Confira também</span><span class="sxs-lookup"><span data-stu-id="823aa-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="823aa-136">**\_TSGatewayServer Win32**</span><span class="sxs-lookup"><span data-stu-id="823aa-136">**Win32\_TSGatewayServer**</span></span>](win32-tsgatewayserver.md)
</dt> </dl>

 

