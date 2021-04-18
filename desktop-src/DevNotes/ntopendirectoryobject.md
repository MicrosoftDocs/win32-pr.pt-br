---
description: Abre um objeto de diretório existente.
ms.assetid: 7313fb32-976b-4c73-b9ba-09fb8ad7faf1
title: Função NtOpenDirectoryObject
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NtOpenDirectoryObject
api_type:
- DllExport
api_location:
- Ntdll.dll
ms.openlocfilehash: ceea03c36e0617e2f48887275e7867e3589c87ae
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105751953"
---
# <a name="ntopendirectoryobject-function"></a><span data-ttu-id="efa8e-103">Função NtOpenDirectoryObject</span><span class="sxs-lookup"><span data-stu-id="efa8e-103">NtOpenDirectoryObject function</span></span>

<span data-ttu-id="efa8e-104">\[Essa função pode ser alterada ou não estar disponível no futuro.\]</span><span class="sxs-lookup"><span data-stu-id="efa8e-104">\[This function may be altered or unavailable in the future.\]</span></span>

<span data-ttu-id="efa8e-105">Abre um objeto de diretório existente.</span><span class="sxs-lookup"><span data-stu-id="efa8e-105">Opens an existing directory object.</span></span>

## <a name="syntax"></a><span data-ttu-id="efa8e-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="efa8e-106">Syntax</span></span>


```C++
NTSTATUS WINAPI NtOpenDirectoryObject(
  _Out_ PHANDLE            DirectoryHandle,
  _In_  ACCESS_MASK        DesiredAccess,
  _In_  POBJECT_ATTRIBUTES ObjectAttributes
);
```



## <a name="parameters"></a><span data-ttu-id="efa8e-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="efa8e-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="efa8e-108">*DirectoryHandle* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="efa8e-108">*DirectoryHandle* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="efa8e-109">Um identificador para o objeto de diretório aberto recentemente.</span><span class="sxs-lookup"><span data-stu-id="efa8e-109">A handle to the newly opened directory object.</span></span>

</dd> <dt>

<span data-ttu-id="efa8e-110">*DesiredAccess* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="efa8e-110">*DesiredAccess* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="efa8e-111">Uma [**\_ máscara de acesso**](../secauthz/access-mask.md) que especifica o acesso solicitado ao objeto de diretório.</span><span class="sxs-lookup"><span data-stu-id="efa8e-111">An [**ACCESS\_MASK**](../secauthz/access-mask.md) that specifies the requested access to the directory object.</span></span> <span data-ttu-id="efa8e-112">Esse parâmetro pode ser um ou mais dos valores a seguir.</span><span class="sxs-lookup"><span data-stu-id="efa8e-112">This parameter can be one or more of the following values.</span></span>



| <span data-ttu-id="efa8e-113">Valor</span><span class="sxs-lookup"><span data-stu-id="efa8e-113">Value</span></span>                                                                                                                                                                                                                                                                      | <span data-ttu-id="efa8e-114">Significado</span><span class="sxs-lookup"><span data-stu-id="efa8e-114">Meaning</span></span>                                                                     |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------|
| <span id="DIRECTORY_QUERY"></span><span id="directory_query"></span><dl> <span data-ttu-id="efa8e-115"><dt>**Do diretório \_**</dt> <dt>0X0001</dt> de consulta</span><span class="sxs-lookup"><span data-stu-id="efa8e-115"><dt>**DIRECTORY\_QUERY**</dt> <dt>0x0001</dt></span></span> </dl>                                            | <span data-ttu-id="efa8e-116">Acesso de consulta ao objeto de diretório.</span><span class="sxs-lookup"><span data-stu-id="efa8e-116">Query access to the directory object.</span></span><br/>                            |
| <span id="DIRECTORY_TRAVERSE"></span><span id="directory_traverse"></span><dl> <span data-ttu-id="efa8e-117"><dt>**Do diretório \_ PERCORRER**</dt> <dt>0x0002</dt></span><span class="sxs-lookup"><span data-stu-id="efa8e-117"><dt>**DIRECTORY\_TRAVERSE**</dt> <dt>0x0002</dt></span></span> </dl>                                   | <span data-ttu-id="efa8e-118">Acesso de pesquisa de nome ao objeto de diretório.</span><span class="sxs-lookup"><span data-stu-id="efa8e-118">Name-lookup access to the directory object.</span></span><br/>                      |
| <span id="DIRECTORY_CREATE_OBJECT"></span><span id="directory_create_object"></span><dl> <span data-ttu-id="efa8e-119"><dt>**Do diretório \_ CRIAR \_**</dt> <dt>0x0004</dt> de objeto</span><span class="sxs-lookup"><span data-stu-id="efa8e-119"><dt>**DIRECTORY\_CREATE\_OBJECT**</dt> <dt>0x0004</dt></span></span> </dl>                   | <span data-ttu-id="efa8e-120">Acesso de criação de nome ao objeto de diretório.</span><span class="sxs-lookup"><span data-stu-id="efa8e-120">Name-creation access to the directory object.</span></span><br/>                    |
| <span id="DIRECTORY_CREATE_SUBDIRECTORY"></span><span id="directory_create_subdirectory"></span><dl> <span data-ttu-id="efa8e-121"><dt>**Do diretório \_ CRIAR \_ subdiretório**</dt> <dt>0x0008</dt></span><span class="sxs-lookup"><span data-stu-id="efa8e-121"><dt>**DIRECTORY\_CREATE\_SUBDIRECTORY**</dt> <dt>0x0008</dt></span></span> </dl> | <span data-ttu-id="efa8e-122">Acesso de criação de subdiretório ao objeto de diretório.</span><span class="sxs-lookup"><span data-stu-id="efa8e-122">Subdirectory-creation access to the directory object.</span></span><br/>            |
| <span id="DIRECTORY_ALL_ACCESS"></span><span id="directory_all_access"></span><dl> <span data-ttu-id="efa8e-123"><dt>**Do diretório \_ Todos \_ os**</dt> <dt>direitos padrão de acesso \_ \_ necessários \| 0xF</dt></span><span class="sxs-lookup"><span data-stu-id="efa8e-123"><dt>**DIRECTORY\_ALL\_ACCESS**</dt> <dt>STANDARD\_RIGHTS\_REQUIRED \| 0xF</dt></span></span> </dl> | <span data-ttu-id="efa8e-124">Todos os direitos anteriores, além **dos \_ direitos padrão \_ necessários**.</span><span class="sxs-lookup"><span data-stu-id="efa8e-124">All of the preceding rights plus **STANDARD\_RIGHTS\_REQUIRED**.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="efa8e-125">*Objetoattributes* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="efa8e-125">*ObjectAttributes* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="efa8e-126">Os atributos para o objeto de diretório.</span><span class="sxs-lookup"><span data-stu-id="efa8e-126">The attributes for the directory object.</span></span> <span data-ttu-id="efa8e-127">Para inicializar a estrutura de **\_ atributos de objeto** , use a macro **InitializeObjectAttributes** .</span><span class="sxs-lookup"><span data-stu-id="efa8e-127">To initialize the **OBJECT\_ATTRIBUTES** structure, use the **InitializeObjectAttributes** macro.</span></span> <span data-ttu-id="efa8e-128">Para obter mais informações, consulte a documentação para esses itens na documentação do WDK.</span><span class="sxs-lookup"><span data-stu-id="efa8e-128">For more information, see the documentation for these items in the documentation for the WDK.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="efa8e-129">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="efa8e-129">Return value</span></span>

<span data-ttu-id="efa8e-130">A função retorna o STATUS \_ êxito ou um status de erro.</span><span class="sxs-lookup"><span data-stu-id="efa8e-130">The function returns STATUS\_SUCCESS or an error status.</span></span> <span data-ttu-id="efa8e-131">Os códigos de status possíveis incluem o seguinte.</span><span class="sxs-lookup"><span data-stu-id="efa8e-131">The possible status codes include the following.</span></span>



| <span data-ttu-id="efa8e-132">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="efa8e-132">Return code</span></span>                                                                                                       | <span data-ttu-id="efa8e-133">Descrição</span><span class="sxs-lookup"><span data-stu-id="efa8e-133">Description</span></span>                                                                                                                                                                                                                                                                                               |
|-------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="efa8e-134"><dt>**STATUS de \_ recursos insuficientes \_**</dt></span><span class="sxs-lookup"><span data-stu-id="efa8e-134"><dt>**STATUS\_INSUFFICIENT\_RESOURCES**</dt></span></span> </dl>    | <span data-ttu-id="efa8e-135">Não foi possível alocar um buffer temporário exigido por essa função.</span><span class="sxs-lookup"><span data-stu-id="efa8e-135">A temporary buffer required by this function could not be allocated.</span></span><br/>                                                                                                                                                                                                                           |
| <dl> <span data-ttu-id="efa8e-136"><dt>**parâmetro de STATUS \_ inválido \_**</dt></span><span class="sxs-lookup"><span data-stu-id="efa8e-136"><dt>**STATUS\_INVALID\_PARAMETER**</dt></span></span> </dl>         | <span data-ttu-id="efa8e-137">O parâmetro objectAttributes especificado era um ponteiro **nulo** , não um ponteiro válido para uma estrutura de **\_ atributos de objeto** ou alguns dos membros especificados na estrutura de **\_ atributos de objeto** não eram válidos.</span><span class="sxs-lookup"><span data-stu-id="efa8e-137">The specified ObjectAttributes parameter was a **NULL** pointer, not a valid pointer to an **OBJECT\_ATTRIBUTES** structure, or some of the members specified in the **OBJECT\_ATTRIBUTES** structure were not valid.</span></span><br/>                                                                          |
| <dl> <span data-ttu-id="efa8e-138"><dt>**nome do objeto de STATUS \_ \_ \_ inválido**</dt></span><span class="sxs-lookup"><span data-stu-id="efa8e-138"><dt>**STATUS\_OBJECT\_NAME\_INVALID**</dt></span></span> </dl>      | <span data-ttu-id="efa8e-139">O parâmetro *objectAttributes* continha um membro **objectname** na estrutura de **\_ atributos de objeto** que não era válida porque uma cadeia de caracteres vazia foi encontrada após o caractere **\_ \_ \_ separador de caminho de nome de objeto** .</span><span class="sxs-lookup"><span data-stu-id="efa8e-139">The *ObjectAttributes* parameter contained an **ObjectName** member in the **OBJECT\_ATTRIBUTES** structure that was not valid because an empty string was found after the **OBJECT\_NAME\_PATH\_SEPARATOR** character.</span></span><br/>                                                                        |
| <dl> <span data-ttu-id="efa8e-140"><dt>**nome do objeto de STATUS \_ \_ \_ não \_ encontrado**</dt></span><span class="sxs-lookup"><span data-stu-id="efa8e-140"><dt>**STATUS\_OBJECT\_NAME\_NOT\_FOUND**</dt></span></span> </dl>   | <span data-ttu-id="efa8e-141">O parâmetro *objectAttributes* continha um membro **objectname** na estrutura de **\_ atributos de objeto** que não pôde ser encontrada.</span><span class="sxs-lookup"><span data-stu-id="efa8e-141">The *ObjectAttributes* parameter contained an **ObjectName** member in the **OBJECT\_ATTRIBUTES** structure that could not be found.</span></span><br/>                                                                                                                                                           |
| <dl> <span data-ttu-id="efa8e-142"><dt>**caminho do objeto de STATUS \_ \_ \_ não \_ encontrado**</dt></span><span class="sxs-lookup"><span data-stu-id="efa8e-142"><dt>**STATUS\_OBJECT\_PATH\_NOT\_FOUND**</dt></span></span> </dl>   | <span data-ttu-id="efa8e-143">O parâmetro *objectAttributes* continha um membro **objectname** na estrutura de **\_ atributos de objeto** com um caminho de objeto que não pôde ser encontrado.</span><span class="sxs-lookup"><span data-stu-id="efa8e-143">The *ObjectAttributes* parameter contained an **ObjectName** member in the **OBJECT\_ATTRIBUTES** structure with an object path that could not be found.</span></span> <br/>                                                                                                                                      |
| <dl> <span data-ttu-id="efa8e-144"><dt>**Status \_ do sintaxe de caminho de objeto \_ \_ \_ inadequada**</dt></span><span class="sxs-lookup"><span data-stu-id="efa8e-144"><dt>**STATUS\_OBJECT\_PATH\_SYNTAX\_BAD** </dt></span></span> </dl> | <span data-ttu-id="efa8e-145">O parâmetro *objectAttributes* não continha um membro **RootDirectory** , mas o membro **objectname** na estrutura de **\_ atributos de objeto** era uma cadeia de caracteres vazia ou não continha um caractere **\_ \_ \_ separador de caminho de nome de objeto** .</span><span class="sxs-lookup"><span data-stu-id="efa8e-145">The *ObjectAttributes* parameter did not contain a **RootDirectory** member, but the **ObjectName** member in the **OBJECT\_ATTRIBUTES** structure was an empty string or did not contain an **OBJECT\_NAME\_PATH\_SEPARATOR** character.</span></span> <span data-ttu-id="efa8e-146">Isso indica uma sintaxe incorreta para o caminho do objeto.</span><span class="sxs-lookup"><span data-stu-id="efa8e-146">This indicates incorrect syntax for the object path.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="efa8e-147">Comentários</span><span class="sxs-lookup"><span data-stu-id="efa8e-147">Remarks</span></span>

<span data-ttu-id="efa8e-148">Esta função não tem biblioteca de importação ou arquivo de cabeçalho associado; Você deve chamá-lo usando as funções [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) e [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) .</span><span class="sxs-lookup"><span data-stu-id="efa8e-148">This function has no associated import library or header file; you must call it using the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) functions.</span></span>

## <a name="requirements"></a><span data-ttu-id="efa8e-149">Requisitos</span><span class="sxs-lookup"><span data-stu-id="efa8e-149">Requirements</span></span>



| <span data-ttu-id="efa8e-150">Requisito</span><span class="sxs-lookup"><span data-stu-id="efa8e-150">Requirement</span></span> | <span data-ttu-id="efa8e-151">Valor</span><span class="sxs-lookup"><span data-stu-id="efa8e-151">Value</span></span> |
|----------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="efa8e-152">DLL</span><span class="sxs-lookup"><span data-stu-id="efa8e-152">DLL</span></span><br/> | <dl> <span data-ttu-id="efa8e-153"><dt>Ntdll.dll</dt></span><span class="sxs-lookup"><span data-stu-id="efa8e-153"><dt>Ntdll.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="efa8e-154">Confira também</span><span class="sxs-lookup"><span data-stu-id="efa8e-154">See also</span></span>

<dl> <dt>

[<span data-ttu-id="efa8e-155">**NtQueryDirectoryObject**</span><span class="sxs-lookup"><span data-stu-id="efa8e-155">**NtQueryDirectoryObject**</span></span>](ntquerydirectoryobject.md)
</dt> </dl>

 

 
