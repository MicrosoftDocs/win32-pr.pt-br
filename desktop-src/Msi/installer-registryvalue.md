---
description: O método REGISTRYVALUE do objeto do instalador lê informações sobre uma chave do Registro especificada de valor.
ms.assetid: 63c258f9-8649-419d-9f79-3681f9f97302
title: Método Installer. REGISTRYVALUE
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Installer.RegistryValue
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: e6da79ff08eebe62ad177119a35bfc29b21c9350
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105748978"
---
# <a name="installerregistryvalue-method"></a><span data-ttu-id="eb143-103">Método Installer. REGISTRYVALUE</span><span class="sxs-lookup"><span data-stu-id="eb143-103">Installer.RegistryValue method</span></span>

<span data-ttu-id="eb143-104">O método **REGISTRYVALUE** do objeto do [**instalador**](installer-object.md) lê informações sobre uma chave do Registro especificada de valor.</span><span class="sxs-lookup"><span data-stu-id="eb143-104">The **RegistryValue** method of the [**Installer**](installer-object.md) object reads information about a specified registry key of value.</span></span> <span data-ttu-id="eb143-105">Se a chave ou o valor especificado não existir, o método retornará um erro de 9, "Subscrito fora do intervalo".</span><span class="sxs-lookup"><span data-stu-id="eb143-105">If the key or value specified does not exist, the method returns an error of 9, "Subscript out of Range."</span></span>

## <a name="syntax"></a><span data-ttu-id="eb143-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="eb143-106">Syntax</span></span>


```JScript
Installer.RegistryValue(
  root,
  key,
  value
)
```



## <a name="parameters"></a><span data-ttu-id="eb143-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="eb143-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="eb143-108">*root*</span><span class="sxs-lookup"><span data-stu-id="eb143-108">*root*</span></span> 
</dt> <dd>

<span data-ttu-id="eb143-109">No Windows NT 4,0, a raiz do registro é uma chave de raiz numérica ou um nome de computador como uma cadeia de caracteres.</span><span class="sxs-lookup"><span data-stu-id="eb143-109">In Windows NT 4.0, the registry root is either a numeric root key or a machine name as a string.</span></span> <span data-ttu-id="eb143-110">Os nomes de máquina são sempre cadeias de caracteres.</span><span class="sxs-lookup"><span data-stu-id="eb143-110">Machine names are always strings.</span></span> <span data-ttu-id="eb143-111">No Windows 95, Windows 98 ou Windows me, a raiz do registro é apenas uma chave de raiz numérica.</span><span class="sxs-lookup"><span data-stu-id="eb143-111">In Windows 95, Windows 98, or Windows Me, the registry root is a numeric root key only.</span></span> <span data-ttu-id="eb143-112">Você só pode acessar HKLM em um computador remoto.</span><span class="sxs-lookup"><span data-stu-id="eb143-112">You can only access HKLM on a remote machine.</span></span>



| <span data-ttu-id="eb143-113">Root</span><span class="sxs-lookup"><span data-stu-id="eb143-113">Root</span></span>                                                                                                                                                                                   | <span data-ttu-id="eb143-114">Significado</span><span class="sxs-lookup"><span data-stu-id="eb143-114">Meaning</span></span>      |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------|
| <span id="HKEY_CLASSES_ROOT"></span><span id="hkey_classes_root"></span><dl> <span data-ttu-id="eb143-115"><dt>**\_raiz de classes hKey \_**</dt></span><span class="sxs-lookup"><span data-stu-id="eb143-115"><dt>**HKEY\_CLASSES\_ROOT**</dt></span></span> </dl>             | <span data-ttu-id="eb143-116">0</span><span class="sxs-lookup"><span data-stu-id="eb143-116">0</span></span><br/> |
| <span id="HKEY_CURRENT_USER"></span><span id="hkey_current_user"></span><dl> <span data-ttu-id="eb143-117"><dt>**HKEY \_ Current \_ User**</dt></span><span class="sxs-lookup"><span data-stu-id="eb143-117"><dt>**HKEY\_CURRENT\_USER**</dt></span></span> </dl>             | <span data-ttu-id="eb143-118">1</span><span class="sxs-lookup"><span data-stu-id="eb143-118">1</span></span><br/> |
| <span id="HKEY_LOCAL_MACHINE"></span><span id="hkey_local_machine"></span><dl> <span data-ttu-id="eb143-119"><dt>**\_máquina local \_ HKEY**</dt></span><span class="sxs-lookup"><span data-stu-id="eb143-119"><dt>**HKEY\_LOCAL\_MACHINE**</dt></span></span> </dl>          | <span data-ttu-id="eb143-120">2</span><span class="sxs-lookup"><span data-stu-id="eb143-120">2</span></span><br/> |
| <span id="HKEY_USERS"></span><span id="hkey_users"></span><dl> <span data-ttu-id="eb143-121"><dt>**usuários de HKEY \_**</dt></span><span class="sxs-lookup"><span data-stu-id="eb143-121"><dt>**HKEY\_USERS**</dt></span></span> </dl>                                   | <span data-ttu-id="eb143-122">3</span><span class="sxs-lookup"><span data-stu-id="eb143-122">3</span></span><br/> |
| <span id="HKEY_PERFORMANCE_DATA"></span><span id="hkey_performance_data"></span><dl> <span data-ttu-id="eb143-123"><dt>**\_dados de desempenho de hKey \_**</dt></span><span class="sxs-lookup"><span data-stu-id="eb143-123"><dt>**HKEY\_PERFORMANCE\_DATA**</dt></span></span> </dl> | <span data-ttu-id="eb143-124">4</span><span class="sxs-lookup"><span data-stu-id="eb143-124">4</span></span><br/> |
| <span id="HKEY_CURRENT_CONFIG"></span><span id="hkey_current_config"></span><dl> <span data-ttu-id="eb143-125"><dt>**\_configuração atual de hKey \_**</dt></span><span class="sxs-lookup"><span data-stu-id="eb143-125"><dt>**HKEY\_CURRENT\_CONFIG**</dt></span></span> </dl>       | <span data-ttu-id="eb143-126">5</span><span class="sxs-lookup"><span data-stu-id="eb143-126">5</span></span><br/> |
| <span id="HKEY_DYN_DATA"></span><span id="hkey_dyn_data"></span><dl> <span data-ttu-id="eb143-127"><dt>**dados do HKEY \_ dyn \_**</dt></span><span class="sxs-lookup"><span data-stu-id="eb143-127"><dt>**HKEY\_DYN\_DATA**</dt></span></span> </dl>                         | <span data-ttu-id="eb143-128">6</span><span class="sxs-lookup"><span data-stu-id="eb143-128">6</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="eb143-129">*chave*</span><span class="sxs-lookup"><span data-stu-id="eb143-129">*key*</span></span> 
</dt> <dd>

<span data-ttu-id="eb143-130">Uma cadeia de caracteres que contém o caminho de chave completo da raiz.</span><span class="sxs-lookup"><span data-stu-id="eb143-130">A string containing the complete key path from the root.</span></span>

</dd> <dt>

<span data-ttu-id="eb143-131">*value*</span><span class="sxs-lookup"><span data-stu-id="eb143-131">*value*</span></span> 
</dt> <dd>

<span data-ttu-id="eb143-132">Esse parâmetro opcional designa qual valor associado deve retornar para a chave especificada.</span><span class="sxs-lookup"><span data-stu-id="eb143-132">This optional parameter designates which associated value to return for the specified key.</span></span> <span data-ttu-id="eb143-133">O valor é um dos valores mostrados na tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="eb143-133">The value is one of the values shown in the following table.</span></span>



| <span data-ttu-id="eb143-134">Valor</span><span class="sxs-lookup"><span data-stu-id="eb143-134">Value</span></span>                                                                                                                                                                                                    | <span data-ttu-id="eb143-135">Significado</span><span class="sxs-lookup"><span data-stu-id="eb143-135">Meaning</span></span>                                                                                                                                                 |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="Missing_or_blank"></span><span id="missing_or_blank"></span><span id="MISSING_OR_BLANK"></span><dl> <span data-ttu-id="eb143-136"><dt>**Ausente ou em branco**</dt></span><span class="sxs-lookup"><span data-stu-id="eb143-136"><dt>**Missing or blank**</dt></span></span> </dl> | <span data-ttu-id="eb143-137">Retorna um valor booleano que indica se a chave existe.</span><span class="sxs-lookup"><span data-stu-id="eb143-137">Returns a Boolean designating whether the key exists.</span></span><br/>                                                                                        |
| <span id="String"></span><span id="string"></span><span id="STRING"></span><dl> <span data-ttu-id="eb143-138"><dt>**Strings**</dt></span><span class="sxs-lookup"><span data-stu-id="eb143-138"><dt>**String**</dt></span></span> </dl>                                         | <span data-ttu-id="eb143-139">Retorna os dados associados ao valor nomeado e falha se o nome do valor for inexistente.</span><span class="sxs-lookup"><span data-stu-id="eb143-139">Returns the data associated with the named value, fails if the value name is non-existent.</span></span><br/>                                                   |
| <span id="Positive_integer"></span><span id="positive_integer"></span><span id="POSITIVE_INTEGER"></span><dl> <span data-ttu-id="eb143-140"><dt>**Inteiro positivo**</dt></span><span class="sxs-lookup"><span data-stu-id="eb143-140"><dt>**Positive integer**</dt></span></span> </dl> | <span data-ttu-id="eb143-141">Retorna o nome do valor enumerado baseado em 1, ele estará vazio se não existir.</span><span class="sxs-lookup"><span data-stu-id="eb143-141">Returns the 1-based enumerated value name, it is empty if non-existent.</span></span> <span data-ttu-id="eb143-142">Essa opção usa a função [**RegEnumValue**](/windows/win32/api/winreg/nf-winreg-regenumvaluea) .</span><span class="sxs-lookup"><span data-stu-id="eb143-142">This option uses the [**RegEnumValue**](/windows/win32/api/winreg/nf-winreg-regenumvaluea) function.</span></span><br/> |
| <span id="Negative_integer"></span><span id="negative_integer"></span><span id="NEGATIVE_INTEGER"></span><dl> <span data-ttu-id="eb143-143"><dt>**Número inteiro negativo**</dt></span><span class="sxs-lookup"><span data-stu-id="eb143-143"><dt>**Negative integer**</dt></span></span> </dl> | <span data-ttu-id="eb143-144">Retorna o nome de subchave enumerado baseado em 1, que estará vazio se não existir.</span><span class="sxs-lookup"><span data-stu-id="eb143-144">Returns the 1-based enumerated subkey name, this is empty if non-existent.</span></span> <span data-ttu-id="eb143-145">Essa opção usa a função [**RegEnumKey**](/windows/win32/api/winreg/nf-winreg-regenumkeya) .</span><span class="sxs-lookup"><span data-stu-id="eb143-145">This option uses the [**RegEnumKey**](/windows/win32/api/winreg/nf-winreg-regenumkeya) function.</span></span><br/>  |
| <span id="Zero_integer"></span><span id="zero_integer"></span><span id="ZERO_INTEGER"></span><dl> <span data-ttu-id="eb143-146"><dt>**Inteiro zero**</dt></span><span class="sxs-lookup"><span data-stu-id="eb143-146"><dt>**Zero integer**</dt></span></span> </dl>                 | <span data-ttu-id="eb143-147">Retorna o nome da classe da cadeia de caracteres para a chave designada.</span><span class="sxs-lookup"><span data-stu-id="eb143-147">Returns the string class name for the designated key.</span></span><br/>                                                                                        |
| <span id="Empty_string____"></span><span id="empty_string____"></span><span id="EMPTY_STRING____"></span><dl> <span data-ttu-id="eb143-148"><dt>**Cadeia de caracteres vazia ""**</dt></span><span class="sxs-lookup"><span data-stu-id="eb143-148"><dt>**Empty string " "**</dt></span></span> </dl> | <span data-ttu-id="eb143-149">Retorna o valor padrão da chave do registro.</span><span class="sxs-lookup"><span data-stu-id="eb143-149">Returns the default value of the registry key.</span></span><br/>                                                                                               |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="eb143-150">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="eb143-150">Return value</span></span>

<span data-ttu-id="eb143-151">Esse método não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="eb143-151">This method does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="eb143-152">Requisitos</span><span class="sxs-lookup"><span data-stu-id="eb143-152">Requirements</span></span>



| <span data-ttu-id="eb143-153">Requisito</span><span class="sxs-lookup"><span data-stu-id="eb143-153">Requirement</span></span> | <span data-ttu-id="eb143-154">Valor</span><span class="sxs-lookup"><span data-stu-id="eb143-154">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="eb143-155">Versão</span><span class="sxs-lookup"><span data-stu-id="eb143-155">Version</span></span><br/> | <span data-ttu-id="eb143-156">Windows Installer 5,0 no Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7.</span><span class="sxs-lookup"><span data-stu-id="eb143-156">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="eb143-157">Windows Installer 4,0 ou Windows Installer 4,5 no Windows Server 2008 ou no Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="eb143-157">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="eb143-158">Windows Installer no Windows Server 2003 ou no Windows XP</span><span class="sxs-lookup"><span data-stu-id="eb143-158">Windows Installer on Windows Server 2003 or Windows XP</span></span><br/> |
| <span data-ttu-id="eb143-159">DLL</span><span class="sxs-lookup"><span data-stu-id="eb143-159">DLL</span></span><br/>     | <dl> <span data-ttu-id="eb143-160"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="eb143-160"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                      |
| <span data-ttu-id="eb143-161">IID</span><span class="sxs-lookup"><span data-stu-id="eb143-161">IID</span></span><br/>     | <span data-ttu-id="eb143-162">IID \_ IInstaller é definido como 000C1090-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="eb143-162">IID\_IInstaller is defined as 000C1090-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                           |



 

 
