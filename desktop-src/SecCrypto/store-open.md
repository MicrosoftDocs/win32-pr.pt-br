---
description: Abre um repositório de certificados especificado.
ms.assetid: d6f398b4-dba6-4d84-b5eb-3c7737d17a6e
title: Método Store. Open
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Store.Open
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: ef4ffe89a4b726ecfa33fb95d213d809cae2487b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105783226"
---
# <a name="storeopen-method"></a><span data-ttu-id="2f4ec-103">Método Store. Open</span><span class="sxs-lookup"><span data-stu-id="2f4ec-103">Store.Open method</span></span>

<span data-ttu-id="2f4ec-104">\[O método **Open** está disponível para uso nos sistemas operacionais especificados na seção requisitos.</span><span class="sxs-lookup"><span data-stu-id="2f4ec-104">\[The **Open** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="2f4ec-105">Em vez disso, use a [**classe X509Store**](/dotnet/api/system.security.cryptography.x509certificates.x509store?view=netcore-3.1) no namespace [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) .\]</span><span class="sxs-lookup"><span data-stu-id="2f4ec-105">Instead, use the [**X509Store Class**](/dotnet/api/system.security.cryptography.x509certificates.x509store?view=netcore-3.1) in the [**System.Security.Cryptography.X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) namespace.\]</span></span>

<span data-ttu-id="2f4ec-106">O método **Open** abre um [*repositório de certificados*](../secgloss/c-gly.md)especificado.</span><span class="sxs-lookup"><span data-stu-id="2f4ec-106">The **Open** method opens a specified [*certificate store*](../secgloss/c-gly.md).</span></span> <span data-ttu-id="2f4ec-107">Por padrão, o local de repositório do usuário atual do CAPICOM \_ \_ e o CAPICOM do repositório de \_ \_ \_ armazenamento são abertos como somente leitura.</span><span class="sxs-lookup"><span data-stu-id="2f4ec-107">By default, the CAPICOM\_CURRENT\_USER\_STORE location and CAPICOM\_MY\_STORE store are opened as read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="2f4ec-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="2f4ec-108">Syntax</span></span>


```VB
Store.Open( _
  [ ByVal StoreLocation ], _
  [ ByVal StoreName ], _
  [ ByVal OpenMode ] _
)
```



## <a name="parameters"></a><span data-ttu-id="2f4ec-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="2f4ec-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2f4ec-110">*StoreLocation* \[ em, opcional\]</span><span class="sxs-lookup"><span data-stu-id="2f4ec-110">*StoreLocation* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="2f4ec-111">Um valor da enumeração [do \_ \_ local de armazenamento capicor](capicom-store-location.md) que indica o local do repositório a ser aberto.</span><span class="sxs-lookup"><span data-stu-id="2f4ec-111">A value of the [CAPICOM\_STORE\_LOCATION](capicom-store-location.md) enumeration that indicates the location of the store to be opened.</span></span> <span data-ttu-id="2f4ec-112">O valor padrão é capicote \_ \_ user \_ Store atual.</span><span class="sxs-lookup"><span data-stu-id="2f4ec-112">The default value is CAPICOM\_CURRENT\_USER\_STORE.</span></span> <span data-ttu-id="2f4ec-113">Esse parâmetro pode usar um dos valores a seguir.</span><span class="sxs-lookup"><span data-stu-id="2f4ec-113">This parameter can be one of the following values.</span></span>



| <span data-ttu-id="2f4ec-114">Valor</span><span class="sxs-lookup"><span data-stu-id="2f4ec-114">Value</span></span>                                                                                                                                                                                                                              | <span data-ttu-id="2f4ec-115">Significado</span><span class="sxs-lookup"><span data-stu-id="2f4ec-115">Meaning</span></span>                                                                                                                                                                                                                                                                            |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="CAPICOM_ACTIVE_DIRECTORY_USER_STORE"></span><span id="capicom_active_directory_user_store"></span><dl> <span data-ttu-id="2f4ec-116"><dt>**armazenamento de usuários do CAPICOM \_ \_ do Active Directory \_ \_**</dt></span><span class="sxs-lookup"><span data-stu-id="2f4ec-116"><dt>**CAPICOM\_ACTIVE\_DIRECTORY\_USER\_STORE**</dt></span></span> </dl> | <span data-ttu-id="2f4ec-117">O repositório é um repositório Active Directory.</span><span class="sxs-lookup"><span data-stu-id="2f4ec-117">The store is an Active Directory store.</span></span> <span data-ttu-id="2f4ec-118">Nenhum erro será gerado se um repositório de Active Directory for aberto como leitura/gravação, mas quaisquer alterações no repositório não serão persistidas.</span><span class="sxs-lookup"><span data-stu-id="2f4ec-118">No error will be generated if an Active Directory store is opened as read/write, but any changes to the store will not be persisted.</span></span> <span data-ttu-id="2f4ec-119">Os certificados não podem ser adicionados ou removidos de repositórios Active Directory.</span><span class="sxs-lookup"><span data-stu-id="2f4ec-119">Certificates cannot be added to or removed from Active Directory stores.</span></span><br/>                   |
| <span id="CAPICOM_CURRENT_USER_STORE"></span><span id="capicom_current_user_store"></span><dl> <span data-ttu-id="2f4ec-120"><dt>**\_armazenamento de \_ usuário \_ atual do CAPICOM**</dt></span><span class="sxs-lookup"><span data-stu-id="2f4ec-120"><dt>**CAPICOM\_CURRENT\_USER\_STORE**</dt></span></span> </dl>                             | <span data-ttu-id="2f4ec-121">O repositório é um armazenamento de usuário atual.</span><span class="sxs-lookup"><span data-stu-id="2f4ec-121">The store is a current user store.</span></span> <span data-ttu-id="2f4ec-122">Um armazenamento de usuário atual pode ser um repositório de leitura/gravação.</span><span class="sxs-lookup"><span data-stu-id="2f4ec-122">A current user store may be a read/write store.</span></span> <span data-ttu-id="2f4ec-123">Se for, as alterações no conteúdo do repositório serão persistidas.</span><span class="sxs-lookup"><span data-stu-id="2f4ec-123">If it is, changes in the contents of the store are persisted.</span></span><br/>                                                                                                                        |
| <span id="CAPICOM_LOCAL_MACHINE_STORE"></span><span id="capicom_local_machine_store"></span><dl> <span data-ttu-id="2f4ec-124"><dt>**CAPICOM do \_ \_ armazenamento do computador local \_**</dt></span><span class="sxs-lookup"><span data-stu-id="2f4ec-124"><dt>**CAPICOM\_LOCAL\_MACHINE\_STORE**</dt></span></span> </dl>                          | <span data-ttu-id="2f4ec-125">O repositório é um repositório do computador local.</span><span class="sxs-lookup"><span data-stu-id="2f4ec-125">The store is a local computer store.</span></span> <span data-ttu-id="2f4ec-126">As lojas de computadores locais poderão ser armazenamentos de leitura/gravação somente se o usuário tiver permissões de leitura/gravação.</span><span class="sxs-lookup"><span data-stu-id="2f4ec-126">Local computer stores can be read/write stores only if the user has read/write permissions.</span></span> <span data-ttu-id="2f4ec-127">Se o usuário tiver permissões de leitura/gravação e se o repositório for aberto como leitura/gravação, as alterações no conteúdo do repositório serão persistidas.</span><span class="sxs-lookup"><span data-stu-id="2f4ec-127">If the user has read/write permissions and if the store is opened read/write, then changes in the contents of the store are persisted.</span></span><br/> |
| <span id="CAPICOM_MEMORY_STORE"></span><span id="capicom_memory_store"></span><dl> <span data-ttu-id="2f4ec-128"><dt>**\_armazenamento de memória CApicom \_**</dt></span><span class="sxs-lookup"><span data-stu-id="2f4ec-128"><dt>**CAPICOM\_MEMORY\_STORE**</dt></span></span> </dl>                                                | <span data-ttu-id="2f4ec-129">O repositório é um repositório de memória.</span><span class="sxs-lookup"><span data-stu-id="2f4ec-129">The store is a memory store.</span></span> <span data-ttu-id="2f4ec-130">As alterações no conteúdo da loja não são persistentes.</span><span class="sxs-lookup"><span data-stu-id="2f4ec-130">Any changes in the contents of the store are not persisted.</span></span><br/>                                                                                                                                                                                |
| <span id="CAPICOM_SMART_CARD_USER_STORE"></span><span id="capicom_smart_card_user_store"></span><dl> <span data-ttu-id="2f4ec-131"><dt>**\_armazenamento de \_ usuário do cartão inteligente \_ CAPICOM \_**</dt></span><span class="sxs-lookup"><span data-stu-id="2f4ec-131"><dt>**CAPICOM\_SMART\_CARD\_USER\_STORE**</dt></span></span> </dl>                   | <span data-ttu-id="2f4ec-132">O repositório é o grupo de cartões inteligentes presentes.</span><span class="sxs-lookup"><span data-stu-id="2f4ec-132">The store is the group of present smart cards.</span></span> <span data-ttu-id="2f4ec-133">Introduzido no CAPICOM 2,0.</span><span class="sxs-lookup"><span data-stu-id="2f4ec-133">Introduced in CAPICOM 2.0.</span></span><br/>                                                                                                                                                                                               |



 

</dd> <dt>

<span data-ttu-id="2f4ec-134">*StoreName* \[ em, opcional\]</span><span class="sxs-lookup"><span data-stu-id="2f4ec-134">*StoreName* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="2f4ec-135">Uma cadeia de caracteres que contém o nome do repositório de certificados do sistema a ser aberto.</span><span class="sxs-lookup"><span data-stu-id="2f4ec-135">A string that contains the name of the system certificate store to be opened.</span></span> <span data-ttu-id="2f4ec-136">O valor padrão é capicore \_ My \_ Store.</span><span class="sxs-lookup"><span data-stu-id="2f4ec-136">The default value is CAPICOM\_MY\_STORE.</span></span> <span data-ttu-id="2f4ec-137">Se o repositório for aberto de um script da Web, o caractere de barra invertida ( \\ ) não será permitido no nome.</span><span class="sxs-lookup"><span data-stu-id="2f4ec-137">If the store is opened from a web script, the backslash (\\) character is not allowed in the name.</span></span> <span data-ttu-id="2f4ec-138">Além dos armazenamentos definidos pelo sistema, os armazenamentos definidos pelo usuário podem ser abertos.</span><span class="sxs-lookup"><span data-stu-id="2f4ec-138">In addition to stores defined by the system, user-defined stores can be opened.</span></span>

<span data-ttu-id="2f4ec-139">Esse parâmetro pode ser um repositório definido pelo usuário ou um dos seguintes repositórios de certificados do sistema.</span><span class="sxs-lookup"><span data-stu-id="2f4ec-139">This parameter can be a user-defined store or one of the following system certificate stores.</span></span>



| <span data-ttu-id="2f4ec-140">Valor</span><span class="sxs-lookup"><span data-stu-id="2f4ec-140">Value</span></span>                                                                                                                                                                            | <span data-ttu-id="2f4ec-141">Significado</span><span class="sxs-lookup"><span data-stu-id="2f4ec-141">Meaning</span></span>                                                                                               |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------|
| <span id="CAPICOM_CA_STORE"></span><span id="capicom_ca_store"></span><dl> <span data-ttu-id="2f4ec-142"><dt>**\_armazenamento de AC CApicom \_**</dt></span><span class="sxs-lookup"><span data-stu-id="2f4ec-142"><dt>**CAPICOM\_CA\_STORE**</dt></span></span> </dl>          | <span data-ttu-id="2f4ec-143">Repositório de AC.</span><span class="sxs-lookup"><span data-stu-id="2f4ec-143">CA store.</span></span> <span data-ttu-id="2f4ec-144">Esse armazenamento é usado para armazenar certificados de AC intermediários.</span><span class="sxs-lookup"><span data-stu-id="2f4ec-144">This store is used to store intermediate CA certificates.</span></span><br/>                        |
| <span id="CAPICOM_MY_STORE"></span><span id="capicom_my_store"></span><dl> <span data-ttu-id="2f4ec-145"><dt>**CAPICOM \_ meu \_ repositório**</dt></span><span class="sxs-lookup"><span data-stu-id="2f4ec-145"><dt>**CAPICOM\_MY\_STORE**</dt></span></span> </dl>          | <span data-ttu-id="2f4ec-146">Meu repositório.</span><span class="sxs-lookup"><span data-stu-id="2f4ec-146">My store.</span></span> <span data-ttu-id="2f4ec-147">Esse armazenamento é usado para certificados pessoais de um usuário.</span><span class="sxs-lookup"><span data-stu-id="2f4ec-147">This store is used for a user's personal certificates.</span></span><br/>                           |
| <span id="CAPICOM_OTHER_STORE"></span><span id="capicom_other_store"></span><dl> <span data-ttu-id="2f4ec-148"><dt>**CAPICOM \_ outro \_ armazenamento**</dt></span><span class="sxs-lookup"><span data-stu-id="2f4ec-148"><dt>**CAPICOM\_OTHER\_STORE**</dt></span></span> </dl> | <span data-ttu-id="2f4ec-149">Catálogo Store.</span><span class="sxs-lookup"><span data-stu-id="2f4ec-149">AddressBook store.</span></span> <span data-ttu-id="2f4ec-150">Esse armazenamento é usado para manter os certificados de outros.</span><span class="sxs-lookup"><span data-stu-id="2f4ec-150">This store is used to keep the certificates of others.</span></span><br/>                  |
| <span id="CAPICOM_ROOT_STORE"></span><span id="capicom_root_store"></span><dl> <span data-ttu-id="2f4ec-151"><dt>**CAPICOM de \_ \_ armazenamento raiz**</dt></span><span class="sxs-lookup"><span data-stu-id="2f4ec-151"><dt>**CAPICOM\_ROOT\_STORE**</dt></span></span> </dl>    | <span data-ttu-id="2f4ec-152">Armazenamento raiz.</span><span class="sxs-lookup"><span data-stu-id="2f4ec-152">Root store.</span></span> <span data-ttu-id="2f4ec-153">Esse armazenamento é usado para armazenar a autoridade de certificação raiz e certificados confiáveis e auto-assinados.</span><span class="sxs-lookup"><span data-stu-id="2f4ec-153">This store is used to store the root CA and self-signed, trusted certificates.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="2f4ec-154">*OpenMode* \[ em, opcional\]</span><span class="sxs-lookup"><span data-stu-id="2f4ec-154">*OpenMode* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="2f4ec-155">Um valor da enumeração [do \_ \_ \_ modo de abertura do armazenamento capicor](capicom-store-open-mode.md) que indica o modo aberto da loja.</span><span class="sxs-lookup"><span data-stu-id="2f4ec-155">A value of the [CAPICOM\_STORE\_OPEN\_MODE](capicom-store-open-mode.md) enumeration that indicates the open mode of the store.</span></span> <span data-ttu-id="2f4ec-156">O valor padrão é capicote \_ Store \_ Open \_ Read \_ only.</span><span class="sxs-lookup"><span data-stu-id="2f4ec-156">The default value is CAPICOM\_STORE\_OPEN\_READ\_ONLY.</span></span> <span data-ttu-id="2f4ec-157">Se o repositório for aberto de um script da Web, esse valor será forçado ao armazenamento CAPICOM \_ \_ abrir \_ \_ somente existente.</span><span class="sxs-lookup"><span data-stu-id="2f4ec-157">If the store is opened from a web script, this value is forced to CAPICOM\_STORE\_OPEN\_EXISTING\_ONLY.</span></span> <span data-ttu-id="2f4ec-158">Esse parâmetro pode usar um dos valores a seguir.</span><span class="sxs-lookup"><span data-stu-id="2f4ec-158">This parameter can be one of the following values.</span></span>



| <span data-ttu-id="2f4ec-159">Valor</span><span class="sxs-lookup"><span data-stu-id="2f4ec-159">Value</span></span>                                                                                                                                                                                                                           | <span data-ttu-id="2f4ec-160">Significado</span><span class="sxs-lookup"><span data-stu-id="2f4ec-160">Meaning</span></span>                                                                                                                           |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------|
| <span id="CAPICOM_STORE_OPEN_MAXIMUM_ALLOWED"></span><span id="capicom_store_open_maximum_allowed"></span><dl> <span data-ttu-id="2f4ec-161"><dt>**\_ \_ \_ máximo permitido de armazenamento \_ de CAPICOM**</dt></span><span class="sxs-lookup"><span data-stu-id="2f4ec-161"><dt>**CAPICOM\_STORE\_OPEN\_MAXIMUM\_ALLOWED**</dt></span></span> </dl> | <span data-ttu-id="2f4ec-162">Abra o repositório no modo de leitura/gravação se o usuário tiver permissões de leitura/gravação; caso contrário, abra o repositório no modo somente leitura.</span><span class="sxs-lookup"><span data-stu-id="2f4ec-162">Open the store in read/write mode if the user has read/write permissions; otherwise, open the store in read-only mode.</span></span><br/> |
| <span id="CAPICOM_STORE_OPEN_READ_ONLY"></span><span id="capicom_store_open_read_only"></span><dl> <span data-ttu-id="2f4ec-163"><dt>**CAPICOM de \_ leitura do armazenamento \_ \_ \_**</dt></span><span class="sxs-lookup"><span data-stu-id="2f4ec-163"><dt>**CAPICOM\_STORE\_OPEN\_READ\_ONLY**</dt></span></span> </dl>                   | <span data-ttu-id="2f4ec-164">Abra o repositório no modo somente leitura.</span><span class="sxs-lookup"><span data-stu-id="2f4ec-164">Open the store in read-only mode.</span></span><br/>                                                                                      |
| <span id="CAPICOM_STORE_OPEN_READ_WRITE"></span><span id="capicom_store_open_read_write"></span><dl> <span data-ttu-id="2f4ec-165"><dt>**o CAPICOM de \_ \_ leitura e \_ \_ gravação aberta**</dt></span><span class="sxs-lookup"><span data-stu-id="2f4ec-165"><dt>**CAPICOM\_STORE\_OPEN\_READ\_WRITE**</dt></span></span> </dl>                | <span data-ttu-id="2f4ec-166">Abra o repositório no modo de leitura/gravação.</span><span class="sxs-lookup"><span data-stu-id="2f4ec-166">Open the store in read/write mode.</span></span><br/>                                                                                     |



 

<span data-ttu-id="2f4ec-167">Os sinalizadores a seguir podem ser combinados com os valores na tabela anterior usando uma operação **or** lógica.</span><span class="sxs-lookup"><span data-stu-id="2f4ec-167">The following flags can be combined with the values in the previous table by using a logical-**OR** operation.</span></span>



| <span data-ttu-id="2f4ec-168">Valor</span><span class="sxs-lookup"><span data-stu-id="2f4ec-168">Value</span></span>                                                                                                                                                                                                                              | <span data-ttu-id="2f4ec-169">Significado</span><span class="sxs-lookup"><span data-stu-id="2f4ec-169">Meaning</span></span>                                                                                     |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------|
| <span id="CAPICOM_STORE_OPEN_EXISTING_ONLY"></span><span id="capicom_store_open_existing_only"></span><dl> <span data-ttu-id="2f4ec-170"><dt>**CAPICOM \_ Store \_ abrir \_ \_ somente existente**</dt></span><span class="sxs-lookup"><span data-stu-id="2f4ec-170"><dt>**CAPICOM\_STORE\_OPEN\_EXISTING\_ONLY**</dt></span></span> </dl>          | <span data-ttu-id="2f4ec-171">Abrir somente repositórios existentes; Não crie um novo repositório.</span><span class="sxs-lookup"><span data-stu-id="2f4ec-171">Open existing stores only; do not create a new store.</span></span> <span data-ttu-id="2f4ec-172">Introduzido no CAPICOM 2,0.</span><span class="sxs-lookup"><span data-stu-id="2f4ec-172">Introduced in CAPICOM 2.0.</span></span><br/> |
| <span id="CAPICOM_STORE_OPEN_INCLUDE_ARCHIVED"></span><span id="capicom_store_open_include_archived"></span><dl> <span data-ttu-id="2f4ec-173"><dt>**o CAPICOM de \_ Store \_ aberto \_ incluem \_ arquivados**</dt></span><span class="sxs-lookup"><span data-stu-id="2f4ec-173"><dt>**CAPICOM\_STORE\_OPEN\_INCLUDE\_ARCHIVED**</dt></span></span> </dl> | <span data-ttu-id="2f4ec-174">Inclua certificados arquivados ao usar o repositório.</span><span class="sxs-lookup"><span data-stu-id="2f4ec-174">Include archived certificates when using the store.</span></span> <span data-ttu-id="2f4ec-175">Introduzido no CAPICOM 2,0.</span><span class="sxs-lookup"><span data-stu-id="2f4ec-175">Introduced in CAPICOM 2.0.</span></span><br/>   |



 

<span data-ttu-id="2f4ec-176">Os repositórios em alguns locais podem ser abertos somente no modo somente leitura.</span><span class="sxs-lookup"><span data-stu-id="2f4ec-176">Stores in some locations can be opened only in read-only mode.</span></span> <span data-ttu-id="2f4ec-177">Isso inclui todas as lojas no \_ repositório do computador local CApicom \_ \_ para o qual o usuário não tem permissões de gravação.</span><span class="sxs-lookup"><span data-stu-id="2f4ec-177">These include all stores in CAPICOM\_LOCAL\_MACHINE\_STORE for which the user does not have write permissions.</span></span> <span data-ttu-id="2f4ec-178">Tenta abrir um repositório como um repositório de leitura/gravação sem acesso adequado e as permissões resultarão na falha do método **Open** .</span><span class="sxs-lookup"><span data-stu-id="2f4ec-178">Attempts to open a store as a read/write store without proper access and permissions will result in the failure of the **Open** method.</span></span> <span data-ttu-id="2f4ec-179">Active Directory armazenamentos podem ser abertos como um repositório de leitura/gravação sem falha do método **Open** , mas as alterações no repositório não serão persistidas.</span><span class="sxs-lookup"><span data-stu-id="2f4ec-179">Active Directory stores can be opened as a read/write store without failure of the **Open** method, but changes to the store will not be persisted.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2f4ec-180">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="2f4ec-180">Return value</span></span>

<span data-ttu-id="2f4ec-181">Esse método não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="2f4ec-181">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="2f4ec-182">Comentários</span><span class="sxs-lookup"><span data-stu-id="2f4ec-182">Remarks</span></span>

<span data-ttu-id="2f4ec-183">Se esse método for chamado em um repositório de cartão inteligente, outras interfaces de usuário de cartão inteligente poderão ser invocadas.</span><span class="sxs-lookup"><span data-stu-id="2f4ec-183">If this method is called on a SmartCard store, additional SmartCard user interfaces may be invoked.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="2f4ec-184">Quando esse método é chamado de um script da Web, o script precisa acessar certificados digitais no computador local.</span><span class="sxs-lookup"><span data-stu-id="2f4ec-184">When this method is called from a web script, the script needs to access digital certificates on the local computer.</span></span> <span data-ttu-id="2f4ec-185">Se você permitir que o script acesse seus certificados digitais, o site do qual o script é executado também obterá acesso a todas as informações pessoais armazenadas nos certificados.</span><span class="sxs-lookup"><span data-stu-id="2f4ec-185">If you allow the script to access your digital certificates, the website from which the script is run will also gain access to any personal information stored in the certificates.</span></span> <span data-ttu-id="2f4ec-186">Na primeira vez que esse método é chamado de um domínio específico, uma caixa de diálogo é gerada na qual o usuário deve indicar se o acesso aos certificados deve ser permitido.</span><span class="sxs-lookup"><span data-stu-id="2f4ec-186">The first time this method is called from a particular domain, a dialog box is generated in which the user must indicate whether access to the certificates should be allowed.</span></span> <span data-ttu-id="2f4ec-187">Lojas abertas de um script da Web automaticamente forçam o sinalizador CAPICOM \_ \_ Open \_ existing Store \_ .</span><span class="sxs-lookup"><span data-stu-id="2f4ec-187">Stores opened from a web script automatically force the CAPICOM\_STORE\_OPEN\_EXISTING\_ONLY flag.</span></span>

 

<span data-ttu-id="2f4ec-188">Se *StoreLocation* for **o \_ \_ armazenamento de \_ usuário \_ do cartão inteligente CAPICOM**, *StoreName* será ignorado.</span><span class="sxs-lookup"><span data-stu-id="2f4ec-188">If *StoreLocation* is **CAPICOM\_SMART\_CARD\_USER\_STORE**, *StoreName* is ignored.</span></span> <span data-ttu-id="2f4ec-189">Nesse caso, o CAPICOM lê todos os certificados de todos os leitores disponíveis que contêm um cartão inteligente.</span><span class="sxs-lookup"><span data-stu-id="2f4ec-189">In this case, CAPICOM reads all certificates from all available readers that contain a smart card.</span></span>

## <a name="requirements"></a><span data-ttu-id="2f4ec-190">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2f4ec-190">Requirements</span></span>



| <span data-ttu-id="2f4ec-191">Requisito</span><span class="sxs-lookup"><span data-stu-id="2f4ec-191">Requirement</span></span> | <span data-ttu-id="2f4ec-192">Valor</span><span class="sxs-lookup"><span data-stu-id="2f4ec-192">Value</span></span> |
|----------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="2f4ec-193">Redistribuível</span><span class="sxs-lookup"><span data-stu-id="2f4ec-193">Redistributable</span></span><br/> | <span data-ttu-id="2f4ec-194">CAPICOM 2,0 ou posterior no Windows Server 2003 e no Windows XP</span><span class="sxs-lookup"><span data-stu-id="2f4ec-194">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="2f4ec-195">DLL</span><span class="sxs-lookup"><span data-stu-id="2f4ec-195">DLL</span></span><br/>             | <dl> <span data-ttu-id="2f4ec-196"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="2f4ec-196"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2f4ec-197">Confira também</span><span class="sxs-lookup"><span data-stu-id="2f4ec-197">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2f4ec-198">**Repositório**</span><span class="sxs-lookup"><span data-stu-id="2f4ec-198">**Store**</span></span>](store.md)
</dt> <dt>

[<span data-ttu-id="2f4ec-199">**Objetos de criptografia**</span><span class="sxs-lookup"><span data-stu-id="2f4ec-199">**Cryptography Objects**</span></span>](cryptography-objects.md)
</dt> <dt>

[<span data-ttu-id="2f4ec-200">**Fechar**</span><span class="sxs-lookup"><span data-stu-id="2f4ec-200">**Close**</span></span>](store-close.md)
</dt> </dl>

 

 
