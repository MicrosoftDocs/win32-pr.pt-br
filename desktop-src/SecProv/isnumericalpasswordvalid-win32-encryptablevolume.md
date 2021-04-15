---
description: Indica se a senha numérica atende aos requisitos de formato especiais para esse valor de autenticação.
ms.assetid: 3995405f-db4d-4f72-98dc-133a09f9cf65
title: Método IsNumericalPasswordValid da classe Win32_EncryptableVolume
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_EncryptableVolume.IsNumericalPasswordValid
api_type:
- COM
api_location:
- Root\CIMV2\Security\MicrosoftVolumeEncryption
ms.openlocfilehash: 7cec4aa31ae9ff6aee90c0f46ded935b3d553783
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105761386"
---
# <a name="isnumericalpasswordvalid-method-of-the-win32_encryptablevolume-class"></a><span data-ttu-id="13d2e-103">Método IsNumericalPasswordValid da classe Win32 \_ EncryptableVolume</span><span class="sxs-lookup"><span data-stu-id="13d2e-103">IsNumericalPasswordValid method of the Win32\_EncryptableVolume class</span></span>

<span data-ttu-id="13d2e-104">O método **IsNumericalPasswordValid** da classe [**Win32 \_ EncryptableVolume**](win32-encryptablevolume.md) indica se a senha numérica atende aos requisitos de formato especiais para esse valor de autenticação.</span><span class="sxs-lookup"><span data-stu-id="13d2e-104">The **IsNumericalPasswordValid** method of the [**Win32\_EncryptableVolume**](win32-encryptablevolume.md) class indicates whether the numerical password meets the special format requirements for this authentication value.</span></span>

## <a name="syntax"></a><span data-ttu-id="13d2e-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="13d2e-105">Syntax</span></span>


```mof
uint32 IsNumericalPasswordValid(
  [in]  string  NumericalPassword,
  [out] boolean IsNumericalPasswordValid
);
```



## <a name="parameters"></a><span data-ttu-id="13d2e-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="13d2e-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="13d2e-107">*NumericalPassword* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="13d2e-107">*NumericalPassword* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="13d2e-108">Tipo: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="13d2e-108">Type: **string**</span></span>

<span data-ttu-id="13d2e-109">Uma cadeia de caracteres que especifica a senha numérica.</span><span class="sxs-lookup"><span data-stu-id="13d2e-109">A string that specifies the numerical password.</span></span>

<span data-ttu-id="13d2e-110">A senha numérica deve conter 48 dígitos.</span><span class="sxs-lookup"><span data-stu-id="13d2e-110">The numerical password must contain 48 digits.</span></span> <span data-ttu-id="13d2e-111">Esses dígitos podem ser divididos em 8 grupos de 6 dígitos, com o último dígito em cada grupo, indicando um valor de soma de verificação para o grupo.</span><span class="sxs-lookup"><span data-stu-id="13d2e-111">These digits can be divided into 8 groups of 6 digits, with the last digit in each group indicating a checksum value for the group.</span></span> <span data-ttu-id="13d2e-112">Cada grupo de 6 dígitos deve ser divisível por 11 e deve ser menor que 720896.</span><span class="sxs-lookup"><span data-stu-id="13d2e-112">Each group of 6 digits must be divisible by 11 and must be less than 720896.</span></span> <span data-ttu-id="13d2e-113">Supondo que um grupo de seis dígitos seja rotulado como X1, X2, X3, x4, X5 e X6, o dígito de soma de verificação X6 é calculado como – X1 + X2 – X3 + X4 – X5 mod 11.</span><span class="sxs-lookup"><span data-stu-id="13d2e-113">Assuming a group of six digits is labeled as x1, x2, x3, x4, x5, and x6, the checksum x6 digit is calculated as –x1+x2–x3+x4–x5 mod 11.</span></span>

<span data-ttu-id="13d2e-114">Os grupos de dígitos podem, opcionalmente, ser separados por um espaço ou hífen.</span><span class="sxs-lookup"><span data-stu-id="13d2e-114">The groups of digits can optionally be separated by a space or hyphen.</span></span> <span data-ttu-id="13d2e-115">Portanto, "XXXXXX-XXXXXX-XXXXXX-XXXXXX-XXXXXX-XXXXXX-XXXXXX-XXXXXX" ou "XXXXXX XXXXXX XXXXXX XXXXXX XXXXXX XXXXXX, XXXXXX XXXXXX", também pode conter senhas numéricas válidas.</span><span class="sxs-lookup"><span data-stu-id="13d2e-115">Therefore, "xxxxxx-xxxxxx-xxxxxx-xxxxxx-xxxxxx-xxxxxx-xxxxxx-xxxxxx" or "xxxxxx xxxxxx xxxxxx xxxxxx xxxxxx xxxxxx xxxxxx xxxxxx" may also contain valid numerical passwords.</span></span>

</dd> <dt>

<span data-ttu-id="13d2e-116">*IsNumericalPasswordValid* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="13d2e-116">*IsNumericalPasswordValid* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="13d2e-117">Tipo: **booliano**</span><span class="sxs-lookup"><span data-stu-id="13d2e-117">Type: **boolean**</span></span>

<span data-ttu-id="13d2e-118">Um valor booliano que será true se a senha numérica atender aos requisitos de formato especiais para esse valor de autenticação; caso contrário, o valor será false.</span><span class="sxs-lookup"><span data-stu-id="13d2e-118">A Boolean value that is true if the numerical password meets the special format requirements for this authentication value, otherwise the value is false.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="13d2e-119">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="13d2e-119">Return value</span></span>

<span data-ttu-id="13d2e-120">Tipo: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="13d2e-120">Type: **uint32**</span></span>

<span data-ttu-id="13d2e-121">Esse método retornará um dos códigos a seguir ou outro código de erro se ele falhar.</span><span class="sxs-lookup"><span data-stu-id="13d2e-121">This method returns one of the following codes or another error code if it fails.</span></span>



| <span data-ttu-id="13d2e-122">Código/valor de retorno</span><span class="sxs-lookup"><span data-stu-id="13d2e-122">Return code/value</span></span>                                                                                                                                 | <span data-ttu-id="13d2e-123">Descrição</span><span class="sxs-lookup"><span data-stu-id="13d2e-123">Description</span></span>                           |
|---------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------|
| <dl> <span data-ttu-id="13d2e-124"><dt>**S \_ OK**</dt> <dt>0 (0x0)</dt></span><span class="sxs-lookup"><span data-stu-id="13d2e-124"><dt>**S\_OK**</dt> <dt>0 (0x0)</dt></span></span> </dl> | <span data-ttu-id="13d2e-125">O método foi bem-sucedido.</span><span class="sxs-lookup"><span data-stu-id="13d2e-125">The method was successful.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="13d2e-126">Comentários</span><span class="sxs-lookup"><span data-stu-id="13d2e-126">Remarks</span></span>

<span data-ttu-id="13d2e-127">Os arquivos de formato MOF (MOF) contêm as definições de classes de Instrumentação de Gerenciamento do Windows (WMI).</span><span class="sxs-lookup"><span data-stu-id="13d2e-127">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="13d2e-128">Os arquivos MOF não são instalados como parte do SDK do Windows.</span><span class="sxs-lookup"><span data-stu-id="13d2e-128">MOF files are not installed as part of the Windows SDK.</span></span> <span data-ttu-id="13d2e-129">Eles são instalados no servidor quando você adiciona a função associada usando o Gerenciador do Servidor.</span><span class="sxs-lookup"><span data-stu-id="13d2e-129">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="13d2e-130">Para obter mais informações sobre arquivos MOF, consulte [formato MOF (MOF)](../wmisdk/managed-object-format--mof-.md).</span><span class="sxs-lookup"><span data-stu-id="13d2e-130">For more information about MOF files, see [Managed Object Format (MOF)](../wmisdk/managed-object-format--mof-.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="13d2e-131">Requisitos</span><span class="sxs-lookup"><span data-stu-id="13d2e-131">Requirements</span></span>



| <span data-ttu-id="13d2e-132">Requisito</span><span class="sxs-lookup"><span data-stu-id="13d2e-132">Requirement</span></span> | <span data-ttu-id="13d2e-133">Valor</span><span class="sxs-lookup"><span data-stu-id="13d2e-133">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="13d2e-134">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="13d2e-134">Minimum supported client</span></span><br/> | <span data-ttu-id="13d2e-135">Windows Vista Enterprise, Windows Vista Ultimate \[ Desktop apps somente\]</span><span class="sxs-lookup"><span data-stu-id="13d2e-135">Windows Vista Enterprise, Windows Vista Ultimate \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="13d2e-136">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="13d2e-136">Minimum supported server</span></span><br/> | <span data-ttu-id="13d2e-137">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="13d2e-137">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="13d2e-138">Namespace</span><span class="sxs-lookup"><span data-stu-id="13d2e-138">Namespace</span></span><br/>                | <span data-ttu-id="13d2e-139">\\MicrosoftVolumeEncryption de \\ segurança \\ cimv2 raiz</span><span class="sxs-lookup"><span data-stu-id="13d2e-139">Root\\CIMV2\\Security\\MicrosoftVolumeEncryption</span></span><br/>                                             |
| <span data-ttu-id="13d2e-140">MOF</span><span class="sxs-lookup"><span data-stu-id="13d2e-140">MOF</span></span><br/>                      | <dl> <span data-ttu-id="13d2e-141"><dt>Win32 \_ encryptablevolume. mof</dt></span><span class="sxs-lookup"><span data-stu-id="13d2e-141"><dt>Win32\_encryptablevolume.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="13d2e-142">Confira também</span><span class="sxs-lookup"><span data-stu-id="13d2e-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="13d2e-143">**\_EncryptableVolume Win32**</span><span class="sxs-lookup"><span data-stu-id="13d2e-143">**Win32\_EncryptableVolume**</span></span>](win32-encryptablevolume.md)
</dt> </dl>

 

 
