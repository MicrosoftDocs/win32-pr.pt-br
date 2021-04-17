---
description: Retorna a chave externa de um arquivo.
ms.assetid: b61b71fb-af6f-4fe3-859b-a9f2f42ca6d2
title: Método GetExternalKeyFromFile da classe Win32_EncryptableVolume
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_EncryptableVolume.GetExternalKeyFromFile
api_type:
- COM
api_location:
- Root\CIMV2\Security\MicrosoftVolumeEncryption
ms.openlocfilehash: ba0c2cf4744c12143090488d730a1d49bab9b431
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105761851"
---
# <a name="getexternalkeyfromfile-method-of-the-win32_encryptablevolume-class"></a><span data-ttu-id="1f0f1-103">Método GetExternalKeyFromFile da classe Win32 \_ EncryptableVolume</span><span class="sxs-lookup"><span data-stu-id="1f0f1-103">GetExternalKeyFromFile method of the Win32\_EncryptableVolume class</span></span>

<span data-ttu-id="1f0f1-104">O método **GetExternalKeyFromFile** da classe [**Win32 \_ EncryptableVolume**](win32-encryptablevolume.md) retorna a chave externa de um arquivo criado pelo [**SaveExternalKeyToFile**](saveexternalkeytofile-win32-encryptablevolume.md), dado o local desse arquivo.</span><span class="sxs-lookup"><span data-stu-id="1f0f1-104">The **GetExternalKeyFromFile** method of the [**Win32\_EncryptableVolume**](win32-encryptablevolume.md) class returns the external key from a file created by [**SaveExternalKeyToFile**](saveexternalkeytofile-win32-encryptablevolume.md), given the location of that file.</span></span>

## <a name="syntax"></a><span data-ttu-id="1f0f1-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="1f0f1-105">Syntax</span></span>


```mof
uint32 GetExternalKeyFromFile(
  [in]  string PathWithFileName,
  [out] uint8  ExternalKey[]
);
```



## <a name="parameters"></a><span data-ttu-id="1f0f1-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="1f0f1-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1f0f1-107">*PathWithFileName* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="1f0f1-107">*PathWithFileName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1f0f1-108">Tipo: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="1f0f1-108">Type: **string**</span></span>

<span data-ttu-id="1f0f1-109">Uma cadeia de caracteres que especifica o local do arquivo que contém uma chave externa.</span><span class="sxs-lookup"><span data-stu-id="1f0f1-109">A string that specifies the location of the file containing an external key.</span></span>

</dd> <dt>

<span data-ttu-id="1f0f1-110">*ExternalKey* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="1f0f1-110">*ExternalKey* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="1f0f1-111">Tipo: **uint8 \[ \]**</span><span class="sxs-lookup"><span data-stu-id="1f0f1-111">Type: **uint8\[\]**</span></span>

<span data-ttu-id="1f0f1-112">Uma matriz de bytes que é a chave externa de 256 bits contida no arquivo que pode ser usada para desbloquear um volume.</span><span class="sxs-lookup"><span data-stu-id="1f0f1-112">An array of bytes that is the 256-bit external key contained within the file that can be used to unlock a volume.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1f0f1-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="1f0f1-113">Return value</span></span>

<span data-ttu-id="1f0f1-114">Tipo: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="1f0f1-114">Type: **uint32**</span></span>

<span data-ttu-id="1f0f1-115">Esse método retornará um dos códigos a seguir ou outro código de erro se ele falhar.</span><span class="sxs-lookup"><span data-stu-id="1f0f1-115">This method returns one of the following codes or another error code if it fails.</span></span>



| <span data-ttu-id="1f0f1-116">Código/valor de retorno</span><span class="sxs-lookup"><span data-stu-id="1f0f1-116">Return code/value</span></span>                                                                                                                                                                   | <span data-ttu-id="1f0f1-117">Descrição</span><span class="sxs-lookup"><span data-stu-id="1f0f1-117">Description</span></span>                                            |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------|
| <dl> <span data-ttu-id="1f0f1-118"><dt>**S \_ OK**</dt> <dt>0 (0x0)</dt></span><span class="sxs-lookup"><span data-stu-id="1f0f1-118"><dt>**S\_OK**</dt> <dt>0 (0x0)</dt></span></span> </dl>                                   | <span data-ttu-id="1f0f1-119">O método foi bem-sucedido.</span><span class="sxs-lookup"><span data-stu-id="1f0f1-119">The method was successful.</span></span><br/>                  |
| <dl> <span data-ttu-id="1f0f1-120"><dt>**E \_ INVALIDARG**</dt> <dt>2147942487 (0x80070057)</dt></span><span class="sxs-lookup"><span data-stu-id="1f0f1-120"><dt>**E\_INVALIDARG**</dt> <dt>2147942487 (0x80070057)</dt></span></span> </dl>           | <span data-ttu-id="1f0f1-121">O arquivo não contém uma chave externa.</span><span class="sxs-lookup"><span data-stu-id="1f0f1-121">The file does not contain an external key.</span></span><br/>  |
| <dl> <span data-ttu-id="1f0f1-122"><dt>**Erro \_ do ARQUIVO \_ não \_ encontrado**</dt> <dt>2147942402 (0x80070002)</dt></span><span class="sxs-lookup"><span data-stu-id="1f0f1-122"><dt>**ERROR\_FILE\_NOT\_FOUND**</dt> <dt>2147942402 (0x80070002)</dt></span></span> </dl> | <span data-ttu-id="1f0f1-123">Não é possível localizar o arquivo no local especificado.</span><span class="sxs-lookup"><span data-stu-id="1f0f1-123">Cannot find file at the location specified.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="1f0f1-124">Comentários</span><span class="sxs-lookup"><span data-stu-id="1f0f1-124">Remarks</span></span>

<span data-ttu-id="1f0f1-125">Os arquivos de formato MOF (MOF) contêm as definições de classes de Instrumentação de Gerenciamento do Windows (WMI).</span><span class="sxs-lookup"><span data-stu-id="1f0f1-125">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="1f0f1-126">Os arquivos MOF não são instalados como parte do SDK do Windows.</span><span class="sxs-lookup"><span data-stu-id="1f0f1-126">MOF files are not installed as part of the Windows SDK.</span></span> <span data-ttu-id="1f0f1-127">Eles são instalados no servidor quando você adiciona a função associada usando o Gerenciador do Servidor.</span><span class="sxs-lookup"><span data-stu-id="1f0f1-127">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="1f0f1-128">Para obter mais informações sobre arquivos MOF, consulte [formato MOF (MOF)](../wmisdk/managed-object-format--mof-.md).</span><span class="sxs-lookup"><span data-stu-id="1f0f1-128">For more information about MOF files, see [Managed Object Format (MOF)](../wmisdk/managed-object-format--mof-.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="1f0f1-129">Requisitos</span><span class="sxs-lookup"><span data-stu-id="1f0f1-129">Requirements</span></span>



| <span data-ttu-id="1f0f1-130">Requisito</span><span class="sxs-lookup"><span data-stu-id="1f0f1-130">Requirement</span></span> | <span data-ttu-id="1f0f1-131">Valor</span><span class="sxs-lookup"><span data-stu-id="1f0f1-131">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1f0f1-132">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="1f0f1-132">Minimum supported client</span></span><br/> | <span data-ttu-id="1f0f1-133">Windows Vista Enterprise, Windows Vista Ultimate \[ Desktop apps somente\]</span><span class="sxs-lookup"><span data-stu-id="1f0f1-133">Windows Vista Enterprise, Windows Vista Ultimate \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="1f0f1-134">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="1f0f1-134">Minimum supported server</span></span><br/> | <span data-ttu-id="1f0f1-135">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="1f0f1-135">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="1f0f1-136">Namespace</span><span class="sxs-lookup"><span data-stu-id="1f0f1-136">Namespace</span></span><br/>                | <span data-ttu-id="1f0f1-137">\\MicrosoftVolumeEncryption de \\ segurança \\ cimv2 raiz</span><span class="sxs-lookup"><span data-stu-id="1f0f1-137">Root\\CIMV2\\Security\\MicrosoftVolumeEncryption</span></span><br/>                                             |
| <span data-ttu-id="1f0f1-138">MOF</span><span class="sxs-lookup"><span data-stu-id="1f0f1-138">MOF</span></span><br/>                      | <dl> <span data-ttu-id="1f0f1-139"><dt>Win32 \_ encryptablevolume. mof</dt></span><span class="sxs-lookup"><span data-stu-id="1f0f1-139"><dt>Win32\_encryptablevolume.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1f0f1-140">Confira também</span><span class="sxs-lookup"><span data-stu-id="1f0f1-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1f0f1-141">**\_EncryptableVolume Win32**</span><span class="sxs-lookup"><span data-stu-id="1f0f1-141">**Win32\_EncryptableVolume**</span></span>](win32-encryptablevolume.md)
</dt> </dl>

 

 
