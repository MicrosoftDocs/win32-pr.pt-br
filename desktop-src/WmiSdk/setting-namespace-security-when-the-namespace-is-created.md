---
title: Definindo a segurança na criação do namespace
description: O arquivo de formato MOF (MOF) que cria um namespace também pode definir os descritores de segurança para o namespace, incluindo o qualificador NamespaceSecuritySDDL com a descrição de segurança no formato SDDL (Security Descriptor Definition Language).
ms.assetid: eeda3351-11ec-4064-90dd-f67ccf5c8cb6
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 461b23dbac3984ffdd49311cbe340ae2b0c5b022
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104506222"
---
# <a name="setting-security-on-namespace-creation"></a><span data-ttu-id="74fa7-103">Definindo a segurança na criação do namespace</span><span class="sxs-lookup"><span data-stu-id="74fa7-103">Setting security on namespace creation</span></span>

<span data-ttu-id="74fa7-104">O arquivo de formato MOF (MOF) que cria um namespace também pode definir os descritores de [*segurança*](/windows/desktop/SecGloss/s-gly) para o namespace, incluindo o qualificador **NamespaceSecuritySDDL** com a descrição de segurança no formato [SDDL (Security Descriptor Definition Language)](/windows/desktop/SecAuthZ/security-descriptor-definition-language) .</span><span class="sxs-lookup"><span data-stu-id="74fa7-104">The Managed Object Format (MOF) file that creates a namespace can also define the [*security descriptors*](/windows/desktop/SecGloss/s-gly) for the namespace by including the **NamespaceSecuritySDDL** qualifier with the security descriptor in [security descriptor definition language (SDDL)](/windows/desktop/SecAuthZ/security-descriptor-definition-language) format.</span></span>

<span data-ttu-id="74fa7-105">Você pode usar o **NamespaceSecuritySDDL** para proteger qualquer namespace.</span><span class="sxs-lookup"><span data-stu-id="74fa7-105">You can use **NamespaceSecuritySDDL** to secure any namespace.</span></span> <span data-ttu-id="74fa7-106">Você também pode usar esse qualificador em um arquivo MOF simples para alterar o descritor de segurança em um namespace existente.</span><span class="sxs-lookup"><span data-stu-id="74fa7-106">You can also use this qualifier in a simple MOF file to alter the security descriptor on an existing namespace.</span></span> <span data-ttu-id="74fa7-107">A cadeia de caracteres SDDL é processada pelo WMI para estabelecer a segurança do namespace, mas não é armazenada como uma cadeia de caracteres.</span><span class="sxs-lookup"><span data-stu-id="74fa7-107">The SDDL string is processed by WMI to establish the namespace security but is not stored as a string.</span></span> <span data-ttu-id="74fa7-108">Se nenhum descritor de segurança for especificado, a segurança padrão será usada.</span><span class="sxs-lookup"><span data-stu-id="74fa7-108">If no security descriptor is specified, the default security is used.</span></span> <span data-ttu-id="74fa7-109">Para obter mais informações, consulte [Configurando descritores de segurança namepace](setting-namespace-security-descriptors.md).</span><span class="sxs-lookup"><span data-stu-id="74fa7-109">For more information, see [Setting Namepace Security Descriptors](setting-namespace-security-descriptors.md).</span></span>

<span data-ttu-id="74fa7-110">O procedimento a seguir define o descritor de segurança para o namespace *\\ MyNamespace raiz* .</span><span class="sxs-lookup"><span data-stu-id="74fa7-110">The following procedure sets the security descriptor for the *root\\MyNamespace* namespace.</span></span> <span data-ttu-id="74fa7-111">A cadeia de caracteres SDDL define o proprietário e o grupo para usuários autenticados e especifica uma [*DACL (lista de controle de acesso discricionário)*](/windows/desktop/SecGloss/d-gly) que é herdada pelos namespaces filho.</span><span class="sxs-lookup"><span data-stu-id="74fa7-111">The SDDL string sets the owner and group to authenticated users and specifies a [*discretionary access control list (DACL)*](/windows/desktop/SecGloss/d-gly) that is inherited by child namespaces.</span></span> <span data-ttu-id="74fa7-112">A DACL permite ao usuário o direito de ler dados, executar métodos, gravar dados em classes de provedor e usar o acesso remoto: **WBEM \_ habilitar**, **\_ método WBEM \_ Execute**, **\_ \_ provedor de gravação WBEM**, **\_ \_ acesso remoto WBEM**.</span><span class="sxs-lookup"><span data-stu-id="74fa7-112">The DACL allows the user the right to read data, execute methods, write data to provider classes and use remote access: **WBEM\_ENABLE**, **WBEM\_METHOD\_EXECUTE**, **WBEM\_WRITE\_PROVIDER**, **WBEM\_REMOTE\_ACCESS**.</span></span> <span data-ttu-id="74fa7-113">Para obter mais informações, consulte [Access to WMI namespaces](access-to-wmi-namespaces.md).</span><span class="sxs-lookup"><span data-stu-id="74fa7-113">For more information, see [Access to WMI Namespaces](access-to-wmi-namespaces.md).</span></span>

<span data-ttu-id="74fa7-114">**Para definir uma DACL de namespace**</span><span class="sxs-lookup"><span data-stu-id="74fa7-114">**To set a namespace DACL**</span></span>

1.  <span data-ttu-id="74fa7-115">Crie um arquivo de formato MOF (MOF) ou modifique o arquivo MOF existente que define o namespace para adicionar o qualificador **NamespaceSecuritySDDL** com a cadeia de caracteres SDDL.</span><span class="sxs-lookup"><span data-stu-id="74fa7-115">Create a Managed Object Format (MOF) file or modify your existing MOF file that defines the namespace to add the **NamespaceSecuritySDDL** qualifier with the SDDL string.</span></span>

    <span data-ttu-id="74fa7-116">O exemplo de código a seguir mostra que o namespace a ser modificado é root \\ MyNamespace e o arquivo é chamado MyNamespace \_ Security. mof.</span><span class="sxs-lookup"><span data-stu-id="74fa7-116">The following code example shows the namespace to be modified is root\\MyNamespace and the file is named MyNamespace\_security.mof.</span></span>

    ```mof
    #pragma autorecover
    #pragma namespace("\\\\.\\root")
    [NamespaceSecuritySDDL ("O:BAG:BAD:(A;CI;0x60003;;;WD)")]
    Instance of __Namespace
    {
      Name = "MyNamespace";
    };
    ```

    

2.  <span data-ttu-id="74fa7-117">Lembre-se de que a cadeia de caracteres SDDL diferencia maiúsculas de minúsculas: as letras devem estar em letras maiúsculas.</span><span class="sxs-lookup"><span data-stu-id="74fa7-117">Be aware that the SDDL string is case-sensitive: the letters must be capitalized.</span></span>

    <span data-ttu-id="74fa7-118">O exemplo de código a seguir mostra as letras "o" e "g" na cadeia de caracteres SDDL como minúsculas e fará com que Mofcomp.exe retorne um erro.</span><span class="sxs-lookup"><span data-stu-id="74fa7-118">The following code example shows the letters "o" and "g" in the SDDL string as lowercase and will cause Mofcomp.exe to return an error.</span></span>

    ```mof
    #pragma autorecover
    #pragma namespace("\\\\.\\root")
    [NamespaceSecuritySDDL("o:BAg:BAD:(A;CI;0x60003;;;WD)")] 
    Instance of __Namespace
    {
      Name = "MyNamespace";
    };
    ```

    

3.  <span data-ttu-id="74fa7-119">Execute [**Mofcomp.exe**](mofcomp.md) para compilar o arquivo MOF.</span><span class="sxs-lookup"><span data-stu-id="74fa7-119">Run [**Mofcomp.exe**](mofcomp.md) to compile the MOF file.</span></span>

    <span data-ttu-id="74fa7-120">**c: \\ Mofcomp MyNamespace \_ Security. mof**</span><span class="sxs-lookup"><span data-stu-id="74fa7-120">**c:\\mofcomp MyNamespace\_security.mof**</span></span>

    <span data-ttu-id="74fa7-121">Em C++, use os métodos [**IMoFCompiler**](/windows/desktop/api/Wbemcli/nn-wbemcli-imofcompiler) .</span><span class="sxs-lookup"><span data-stu-id="74fa7-121">In C++, use the [**IMoFCompiler**](/windows/desktop/api/Wbemcli/nn-wbemcli-imofcompiler) methods.</span></span>

4.  <span data-ttu-id="74fa7-122">Se a tentativa de definir a DACL do namespace falhar, considere as seguintes mensagens de erro:</span><span class="sxs-lookup"><span data-stu-id="74fa7-122">If your attempt to set the namespace DACL fails, consider the following error messages:</span></span>

    

    | <span data-ttu-id="74fa7-123">Erro</span><span class="sxs-lookup"><span data-stu-id="74fa7-123">Error</span></span>                           | <span data-ttu-id="74fa7-124">Descrição</span><span class="sxs-lookup"><span data-stu-id="74fa7-124">Description</span></span>                                                                                                  |
    |---------------------------------|--------------------------------------------------------------------------------------------------------------|
    | <span data-ttu-id="74fa7-125">**parâmetro de WBEM \_ E \_ inválido \_**</span><span class="sxs-lookup"><span data-stu-id="74fa7-125">**WBEM\_E\_INVALID\_PARAMETER**</span></span> | <span data-ttu-id="74fa7-126">Não há nenhuma DACL herdada.</span><span class="sxs-lookup"><span data-stu-id="74fa7-126">There is no inherited DACL.</span></span> <span data-ttu-id="74fa7-127">Como alternativa, o chamador violou a DACL ou o SD no namespace pai.</span><span class="sxs-lookup"><span data-stu-id="74fa7-127">Alternately, the caller has violated the DACL or the SD in the parent namespace.</span></span> |
    | <span data-ttu-id="74fa7-128">**acesso ao WBEM \_ E \_ \_ negado**</span><span class="sxs-lookup"><span data-stu-id="74fa7-128">**WBEM\_E\_ACCESS\_DENIED**</span></span>     | <span data-ttu-id="74fa7-129">O chamador não tem permissão para atualizar o SDDL no MOF.</span><span class="sxs-lookup"><span data-stu-id="74fa7-129">The caller does not have permission to update the SDDL in MOF.</span></span>                                               |

    

     

## <a name="related-topics"></a><span data-ttu-id="74fa7-130">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="74fa7-130">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="74fa7-131">Definindo descritores de segurança de namespace</span><span class="sxs-lookup"><span data-stu-id="74fa7-131">Setting Namespace Security Descriptors</span></span>](setting-namespace-security-descriptors.md)
</dt> <dt>

[<span data-ttu-id="74fa7-132">**Constantes de direitos de acesso de namespace**</span><span class="sxs-lookup"><span data-stu-id="74fa7-132">**Namespace Access Rights Constants**</span></span>](namespace-access-rights-constants.md)
</dt> <dt>

[<span data-ttu-id="74fa7-133">**Constantes do sinalizador ACE do namespace**</span><span class="sxs-lookup"><span data-stu-id="74fa7-133">**Namespace ACE Flag Constants**</span></span>](namespace-ace-flag-constants.md)
</dt> <dt>

[<span data-ttu-id="74fa7-134">Alterando a segurança de acesso em objetos protegíveis</span><span class="sxs-lookup"><span data-stu-id="74fa7-134">Changing Access Security on Securable Objects</span></span>](changing-access-security-on-securable-objects.md)
</dt> </dl>

 

 
