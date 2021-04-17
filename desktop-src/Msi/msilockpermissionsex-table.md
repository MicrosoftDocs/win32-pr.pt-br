---
description: A tabela MsiLockPermissionsEx pode ser usada para proteger serviços, arquivos, chaves do registro e pastas criadas.
ms.assetid: c642f02d-07fa-463f-8151-769c28a71a5c
title: Tabela MsiLockPermissionsEx
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 63d7c63e27d7a9c390e6015eb0ebe5f663de5b4c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105759650"
---
# <a name="msilockpermissionsex-table"></a><span data-ttu-id="e3b8f-103">Tabela MsiLockPermissionsEx</span><span class="sxs-lookup"><span data-stu-id="e3b8f-103">MsiLockPermissionsEx Table</span></span>

<span data-ttu-id="e3b8f-104">A tabela MsiLockPermissionsEx pode ser usada para proteger serviços, arquivos, chaves do registro e pastas criadas.</span><span class="sxs-lookup"><span data-stu-id="e3b8f-104">The MsiLockPermissionsEx Table can be used to secure services, files, registry keys, and created folders.</span></span>

<span data-ttu-id="e3b8f-105">Um pacote não deve conter a tabela MsiLockPermissionsEx e a [Tabela LockPermissions](lockpermissions-table.md).</span><span class="sxs-lookup"><span data-stu-id="e3b8f-105">A package should not contain both the MsiLockPermissionsEx Table and the [LockPermissions Table](lockpermissions-table.md).</span></span>

<span data-ttu-id="e3b8f-106">**[Windows Installer 4,5 ou anterior](not-supported-in-windows-installer-4-5.md):** Sem suporte.</span><span class="sxs-lookup"><span data-stu-id="e3b8f-106">**[Windows Installer 4.5 or earlier](not-supported-in-windows-installer-4-5.md):** Not supported.</span></span> <span data-ttu-id="e3b8f-107">Esta tabela é recomendada para pacotes destinados à instalação com o Windows Installer 5,0 ou posterior.</span><span class="sxs-lookup"><span data-stu-id="e3b8f-107">This table is recommended for packages intended for installation with Windows Installer 5.0 or later.</span></span>

<span data-ttu-id="e3b8f-108">A tabela MsiLockPermissionsEx tem as colunas a seguir.</span><span class="sxs-lookup"><span data-stu-id="e3b8f-108">The MsiLockPermissionsEx Table has the following columns.</span></span>



| <span data-ttu-id="e3b8f-109">Coluna</span><span class="sxs-lookup"><span data-stu-id="e3b8f-109">Column</span></span>               | <span data-ttu-id="e3b8f-110">Tipo</span><span class="sxs-lookup"><span data-stu-id="e3b8f-110">Type</span></span>                                       | <span data-ttu-id="e3b8f-111">Chave</span><span class="sxs-lookup"><span data-stu-id="e3b8f-111">Key</span></span> | <span data-ttu-id="e3b8f-112">Nullable</span><span class="sxs-lookup"><span data-stu-id="e3b8f-112">Nullable</span></span> |
|----------------------|--------------------------------------------|-----|----------|
| <span data-ttu-id="e3b8f-113">MsiLockPermissionsEx</span><span class="sxs-lookup"><span data-stu-id="e3b8f-113">MsiLockPermissionsEx</span></span> | [<span data-ttu-id="e3b8f-114">Text</span><span class="sxs-lookup"><span data-stu-id="e3b8f-114">Text</span></span>](text.md)                           | <span data-ttu-id="e3b8f-115">S</span><span class="sxs-lookup"><span data-stu-id="e3b8f-115">Y</span></span>   | <span data-ttu-id="e3b8f-116">N</span><span class="sxs-lookup"><span data-stu-id="e3b8f-116">N</span></span>        |
| <span data-ttu-id="e3b8f-117">LockObject</span><span class="sxs-lookup"><span data-stu-id="e3b8f-117">LockObject</span></span>           | [<span data-ttu-id="e3b8f-118">Identificador</span><span class="sxs-lookup"><span data-stu-id="e3b8f-118">Identifier</span></span>](identifier.md)               | <span data-ttu-id="e3b8f-119">N</span><span class="sxs-lookup"><span data-stu-id="e3b8f-119">N</span></span>   | <span data-ttu-id="e3b8f-120">N</span><span class="sxs-lookup"><span data-stu-id="e3b8f-120">N</span></span>        |
| <span data-ttu-id="e3b8f-121">Tabela</span><span class="sxs-lookup"><span data-stu-id="e3b8f-121">Table</span></span>                | [<span data-ttu-id="e3b8f-122">Text</span><span class="sxs-lookup"><span data-stu-id="e3b8f-122">Text</span></span>](text.md)                           | <span data-ttu-id="e3b8f-123">N</span><span class="sxs-lookup"><span data-stu-id="e3b8f-123">N</span></span>   | <span data-ttu-id="e3b8f-124">N</span><span class="sxs-lookup"><span data-stu-id="e3b8f-124">N</span></span>        |
| <span data-ttu-id="e3b8f-125">SDDLText</span><span class="sxs-lookup"><span data-stu-id="e3b8f-125">SDDLText</span></span>             | [<span data-ttu-id="e3b8f-126">FormattedSDDLText</span><span class="sxs-lookup"><span data-stu-id="e3b8f-126">FormattedSDDLText</span></span>](formattedsddltext.md) | <span data-ttu-id="e3b8f-127">N</span><span class="sxs-lookup"><span data-stu-id="e3b8f-127">N</span></span>   | <span data-ttu-id="e3b8f-128">N</span><span class="sxs-lookup"><span data-stu-id="e3b8f-128">N</span></span>        |
| <span data-ttu-id="e3b8f-129">Condição</span><span class="sxs-lookup"><span data-stu-id="e3b8f-129">Condition</span></span>            | [<span data-ttu-id="e3b8f-130">Condição</span><span class="sxs-lookup"><span data-stu-id="e3b8f-130">Condition</span></span>](condition.md)                 | <span data-ttu-id="e3b8f-131">N</span><span class="sxs-lookup"><span data-stu-id="e3b8f-131">N</span></span>   | <span data-ttu-id="e3b8f-132">S</span><span class="sxs-lookup"><span data-stu-id="e3b8f-132">Y</span></span>        |



 

## <a name="columns"></a><span data-ttu-id="e3b8f-133">Colunas</span><span class="sxs-lookup"><span data-stu-id="e3b8f-133">Columns</span></span>

<dl> <dt>

<span data-ttu-id="e3b8f-134"><span id="MsiLockPermissionsEx"></span><span id="msilockpermissionsex"></span><span id="MSILOCKPERMISSIONSEX"></span>MsiLockPermissionsEx</span><span class="sxs-lookup"><span data-stu-id="e3b8f-134"><span id="MsiLockPermissionsEx"></span><span id="msilockpermissionsex"></span><span id="MSILOCKPERMISSIONSEX"></span>MsiLockPermissionsEx</span></span>
</dt> <dd>

<span data-ttu-id="e3b8f-135">Esta é a chave primária desta tabela.</span><span class="sxs-lookup"><span data-stu-id="e3b8f-135">This is the primary key of this table.</span></span>

</dd> <dt>

<span data-ttu-id="e3b8f-136"><span id="LockObject"></span><span id="lockobject"></span><span id="LOCKOBJECT"></span>LockObject</span><span class="sxs-lookup"><span data-stu-id="e3b8f-136"><span id="LockObject"></span><span id="lockobject"></span><span id="LOCKOBJECT"></span>LockObject</span></span>
</dt> <dd>

<span data-ttu-id="e3b8f-137">Essa coluna e a coluna da tabela juntas especificam o arquivo, o diretório, a chave do registro ou o serviço a ser protegido.</span><span class="sxs-lookup"><span data-stu-id="e3b8f-137">This column and the Table column together specify the file, directory, registry key, or service that is to be secured.</span></span> <span data-ttu-id="e3b8f-138">A coluna lockobject é uma chave estrangeira que aponta para a chave primária da tabela especificada pela coluna da tabela.</span><span class="sxs-lookup"><span data-stu-id="e3b8f-138">The LockObject column is a foreign key that points to the primary key of the table specified by the Table column.</span></span>

</dd> <dt>

<span data-ttu-id="e3b8f-139"><span id="Table"></span><span id="table"></span><span id="TABLE"></span>Tabela</span><span class="sxs-lookup"><span data-stu-id="e3b8f-139"><span id="Table"></span><span id="table"></span><span id="TABLE"></span>Table</span></span>
</dt> <dd>

<span data-ttu-id="e3b8f-140">Essa coluna e a coluna lockobject especificam o arquivo, o diretório, a chave do registro ou o serviço a ser protegido.</span><span class="sxs-lookup"><span data-stu-id="e3b8f-140">This column and the LockObject column specify the file, directory, registry key, or service that is to be secured.</span></span> <span data-ttu-id="e3b8f-141">Na coluna da tabela, insira arquivo, registro, CreateFolder ou instalar para especificar um lockobject listado na tabela de [arquivos](file-table.md), na [tabela do registro](registry-table.md), na tabela [CreateFolder](createfolder-table.md)ou na [tabela de instalação](serviceinstall-table.md).</span><span class="sxs-lookup"><span data-stu-id="e3b8f-141">In the Table column, enter File, Registry, CreateFolder, or ServiceInstall to specify a LockObject listed in the [File Table](file-table.md), [Registry Table](registry-table.md), [CreateFolder Table](createfolder-table.md), or [ServiceInstall Table](serviceinstall-table.md).</span></span>

</dd> <dt>

<span data-ttu-id="e3b8f-142"><span id="SDDLText"></span><span id="sddltext"></span><span id="SDDLTEXT"></span>SDDLText</span><span class="sxs-lookup"><span data-stu-id="e3b8f-142"><span id="SDDLText"></span><span id="sddltext"></span><span id="SDDLTEXT"></span>SDDLText</span></span>
</dt> <dd>

<span data-ttu-id="e3b8f-143">Insira a cadeia de caracteres SDDL para indicar as permissões a serem aplicadas ao objeto selecionado.</span><span class="sxs-lookup"><span data-stu-id="e3b8f-143">Enter the SDDL string to indicate permissions to apply to selected object.</span></span> <span data-ttu-id="e3b8f-144">O SDDL deve ser fornecido no [formato de cadeia de caracteres do descritor de segurança](../secauthz/security-descriptor-string-format.md).</span><span class="sxs-lookup"><span data-stu-id="e3b8f-144">The SDDL must be provided in [Security Descriptor String Format](../secauthz/security-descriptor-string-format.md).</span></span>

<span data-ttu-id="e3b8f-145">Isso não oferece suporte a propriedades privadas ou públicas.</span><span class="sxs-lookup"><span data-stu-id="e3b8f-145">This does not support private or public properties.</span></span>

</dd> <dt>

<span data-ttu-id="e3b8f-146"><span id="Condition"></span><span id="condition"></span><span id="CONDITION"></span>Problema</span><span class="sxs-lookup"><span data-stu-id="e3b8f-146"><span id="Condition"></span><span id="condition"></span><span id="CONDITION"></span>Condition</span></span>
</dt> <dd>

<span data-ttu-id="e3b8f-147">Esta coluna contém uma expressão condicional usada para determinar se a permissão especificada deve ser aplicada.</span><span class="sxs-lookup"><span data-stu-id="e3b8f-147">This column contains a conditional expression used to determine whether to apply the specified permission.</span></span> <span data-ttu-id="e3b8f-148">Se a condição for avaliada como **false**, a permissão não será aplicada.</span><span class="sxs-lookup"><span data-stu-id="e3b8f-148">If the condition evaluates to **FALSE**, the permission is not applied.</span></span> <span data-ttu-id="e3b8f-149">Se a condição for avaliada como **true**, a permissão será aplicada.</span><span class="sxs-lookup"><span data-stu-id="e3b8f-149">If the condition evaluates to **TRUE**, the permission is applied.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="e3b8f-150">Comentários</span><span class="sxs-lookup"><span data-stu-id="e3b8f-150">Remarks</span></span>

<span data-ttu-id="e3b8f-151">Consulte [protegendo recursos](securing-resources-.md)para obter mais informações sobre como proteger serviços, arquivos, chaves do registro e pastas criadas.</span><span class="sxs-lookup"><span data-stu-id="e3b8f-151">See [Securing Resources](securing-resources-.md)for more information about securing services, files, registry keys, and created folders.</span></span>

<span data-ttu-id="e3b8f-152">Use a tabela MsiLockPermissionsEx para proteger objetos para uma conta de usuário que está sendo criada durante a instalação.</span><span class="sxs-lookup"><span data-stu-id="e3b8f-152">Use the MsiLockPermissionsEx Table to secure objects for a user account that is being created during the installation.</span></span> <span data-ttu-id="e3b8f-153">A conta de usuário já deve existir quando a instalação proteger o objeto.</span><span class="sxs-lookup"><span data-stu-id="e3b8f-153">The user account must already exist when the installation secures the object.</span></span> <span data-ttu-id="e3b8f-154">Crie a conta de usuário antes de instalar o arquivo, a chave do registro, a pasta ou o serviço que está sendo protegido.</span><span class="sxs-lookup"><span data-stu-id="e3b8f-154">Create the user account before installing the file, registry key, folder or service being secured.</span></span>

<span data-ttu-id="e3b8f-155">Se um lockobject e um par de tabelas nesta tabela tiverem mais de uma expressão condicional avaliada como true, a instalação falhará e Windows Installer retornará uma mensagem de erro 1942.</span><span class="sxs-lookup"><span data-stu-id="e3b8f-155">If a LockObject and Table pair in this table has more than one conditional expression that evaluates to true, the installation fails and Windows Installer returns an error message 1942.</span></span>

<span data-ttu-id="e3b8f-156">Se a cadeia de caracteres [FormattedSDDLText](formattedsddltext.md) no campo SDDLText não puder ser resolvida em uma cadeia de caracteres SDDL válida, a instalação falhará e Windows Installer retornará uma mensagem de erro 1943.</span><span class="sxs-lookup"><span data-stu-id="e3b8f-156">If the [FormattedSDDLText](formattedsddltext.md) string in the SDDLText field cannot be resolved into a valid SDDL string, the installation fails and Windows Installer returns an error message 1943.</span></span>

<span data-ttu-id="e3b8f-157">Se o usuário não tiver privilégios suficientes para definir o descritor de segurança especificado pelo campo SDDLText em um arquivo ou pasta, a instalação falhará e Windows Installer retornará uma mensagem de erro 1926.</span><span class="sxs-lookup"><span data-stu-id="e3b8f-157">If the user does not have sufficient privileges to set the security descriptor specified by the SDDLText field on a file or folder, the installation fails and Windows Installer returns an error message 1926.</span></span>

<span data-ttu-id="e3b8f-158">Se o usuário não tiver privilégios suficientes para definir o descritor de segurança especificado pelo campo SDDLText em uma chave do registro, a instalação falhará e Windows Installer retornará uma mensagem de erro 1401.</span><span class="sxs-lookup"><span data-stu-id="e3b8f-158">If the user does not have sufficient privileges to set the security descriptor specified by the SDDLText field on a registry key, the installation fails and Windows Installer returns an error message 1401.</span></span>

<span data-ttu-id="e3b8f-159">Se o usuário não tiver privilégios suficientes para definir o descritor de segurança especificado pelo campo SDDLText em um serviço, a instalação falhará e Windows Installer retornará uma mensagem de erro 1944.</span><span class="sxs-lookup"><span data-stu-id="e3b8f-159">If the user does not have sufficient privileges to set the security descriptor specified by the SDDLText field on a service, the installation fails and Windows Installer returns an error message 1944.</span></span>

## <a name="validation"></a><span data-ttu-id="e3b8f-160">Validação</span><span class="sxs-lookup"><span data-stu-id="e3b8f-160">Validation</span></span>

<dl>

[<span data-ttu-id="e3b8f-161">ICE104</span><span class="sxs-lookup"><span data-stu-id="e3b8f-161">ICE104</span></span>](ice-104.md)  
[<span data-ttu-id="e3b8f-162">ICE03</span><span class="sxs-lookup"><span data-stu-id="e3b8f-162">ICE03</span></span>](ice03.md)  
[<span data-ttu-id="e3b8f-163">ICE06</span><span class="sxs-lookup"><span data-stu-id="e3b8f-163">ICE06</span></span>](ice06.md)  
</dl>

 

 
