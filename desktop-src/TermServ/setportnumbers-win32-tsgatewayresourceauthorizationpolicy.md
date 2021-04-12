---
title: Método setportnumbers da classe Win32_TSGatewayResourceAuthorizationPolicy
description: Define os números de porta que têm permissão para se conectar ao recurso por meio do gateway de Área de Trabalho Remota (Gateway RD).
ms.assetid: f8237ec3-84dc-44f8-ad86-54c46be1fd03
ms.tgt_platform: multiple
keywords:
- Método setportnumbers Serviços de Área de Trabalho Remota
- Método setportnumbers Serviços de Área de Trabalho Remota, classe Win32_TSGatewayResourceAuthorizationPolicy
- Classe Win32_TSGatewayResourceAuthorizationPolicy Serviços de Área de Trabalho Remota, método setportnumbers
topic_type:
- apiref
api_name:
- Win32_TSGatewayResourceAuthorizationPolicy.SetPortNumbers
api_location:
- AagWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b938435abab23e3ad27cf13dbe65e64b9ec859eb
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104455481"
---
# <a name="setportnumbers-method-of-the-win32_tsgatewayresourceauthorizationpolicy-class"></a><span data-ttu-id="c5bdd-106">Método setportnumbers da classe Win32 \_ TSGatewayResourceAuthorizationPolicy</span><span class="sxs-lookup"><span data-stu-id="c5bdd-106">SetPortNumbers method of the Win32\_TSGatewayResourceAuthorizationPolicy class</span></span>

<span data-ttu-id="c5bdd-107">Define os números de porta que têm permissão para se conectar ao recurso por meio do gateway de Área de Trabalho Remota (Gateway RD).</span><span class="sxs-lookup"><span data-stu-id="c5bdd-107">Sets the port numbers that are allowed to connect to the resource through Remote Desktop Gateway (RD Gateway).</span></span>

## <a name="syntax"></a><span data-ttu-id="c5bdd-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="c5bdd-108">Syntax</span></span>


```mof
uint32 SetPortNumbers(
  [in] string PortNumbers
);
```



## <a name="parameters"></a><span data-ttu-id="c5bdd-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="c5bdd-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c5bdd-110">*Portnumbers* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="c5bdd-110">*PortNumbers* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c5bdd-111">Lista de números de porta separados por ponto e vírgula permitidos para este Área de Trabalho Remota RD RAP (política de autorização de recursos).</span><span class="sxs-lookup"><span data-stu-id="c5bdd-111">List of semicolon-separated port numbers that are allowed for this Remote Desktop resource authorization policy (RD RAP).</span></span> <span data-ttu-id="c5bdd-112">Para permitir qualquer número de porta, defina " \* ".</span><span class="sxs-lookup"><span data-stu-id="c5bdd-112">To allow any port number, set "\*".</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="c5bdd-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="c5bdd-113">Remarks</span></span>

<span data-ttu-id="c5bdd-114">Os arquivos de formato MOF (MOF) contêm as definições de classes de Instrumentação de Gerenciamento do Windows (WMI).</span><span class="sxs-lookup"><span data-stu-id="c5bdd-114">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="c5bdd-115">Os arquivos MOF não são instalados como parte do SDK (Software Development Kit) do Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="c5bdd-115">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="c5bdd-116">Eles são instalados no servidor quando você adiciona a função associada usando o Gerenciador do Servidor.</span><span class="sxs-lookup"><span data-stu-id="c5bdd-116">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="c5bdd-117">Para obter mais informações sobre arquivos MOF, consulte [formato MOF (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="c5bdd-117">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="c5bdd-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c5bdd-118">Requirements</span></span>



| <span data-ttu-id="c5bdd-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="c5bdd-119">Requirement</span></span> | <span data-ttu-id="c5bdd-120">Valor</span><span class="sxs-lookup"><span data-stu-id="c5bdd-120">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="c5bdd-121">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="c5bdd-121">Minimum supported client</span></span><br/> | <span data-ttu-id="c5bdd-122">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="c5bdd-122">None supported</span></span><br/>                                                                |
| <span data-ttu-id="c5bdd-123">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="c5bdd-123">Minimum supported server</span></span><br/> | <span data-ttu-id="c5bdd-124">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="c5bdd-124">Windows Server 2008</span></span><br/>                                                           |
| <span data-ttu-id="c5bdd-125">Namespace</span><span class="sxs-lookup"><span data-stu-id="c5bdd-125">Namespace</span></span><br/>                | <span data-ttu-id="c5bdd-126">\\TerminalServices da CIMv2 raiz \\</span><span class="sxs-lookup"><span data-stu-id="c5bdd-126">Root\\CIMv2\\TerminalServices</span></span><br/>                                                 |
| <span data-ttu-id="c5bdd-127">MOF</span><span class="sxs-lookup"><span data-stu-id="c5bdd-127">MOF</span></span><br/>                      | <dl> <span data-ttu-id="c5bdd-128"><dt>TS. mof</dt></span><span class="sxs-lookup"><span data-stu-id="c5bdd-128"><dt>TSGateway.mof</dt></span></span> </dl> |
| <span data-ttu-id="c5bdd-129">DLL</span><span class="sxs-lookup"><span data-stu-id="c5bdd-129">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c5bdd-130"><dt>AagWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c5bdd-130"><dt>AagWmi.dll</dt></span></span> </dl>    |



## <a name="see-also"></a><span data-ttu-id="c5bdd-131">Confira também</span><span class="sxs-lookup"><span data-stu-id="c5bdd-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c5bdd-132">**\_TSGatewayResourceAuthorizationPolicy Win32**</span><span class="sxs-lookup"><span data-stu-id="c5bdd-132">**Win32\_TSGatewayResourceAuthorizationPolicy**</span></span>](win32-tsgatewayresourceauthorizationpolicy.md)
</dt> </dl>

 

