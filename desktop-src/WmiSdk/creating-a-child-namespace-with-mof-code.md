---
description: A maneira mais simples de criar um namespace é usar o código formato MOF (MOF) para criar o namespace dentro do diretório atual. O diretório atual é definido quando você faz logon.
ms.assetid: 2b83cd96-079f-4178-9e5a-68ede3a92066
ms.tgt_platform: multiple
title: Criando um namespace filho com código MOF
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7f80aa04e2ef4f5c7bbfc43d9020727b3b2a6e0d
ms.sourcegitcommit: b7a1da2711221fa99072079bf52399cbdfc6bd9d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/05/2021
ms.locfileid: "104011964"
---
# <a name="creating-a-child-namespace-with-mof-code"></a><span data-ttu-id="9751a-104">Criando um namespace filho com código MOF</span><span class="sxs-lookup"><span data-stu-id="9751a-104">Creating a Child Namespace with MOF Code</span></span>

<span data-ttu-id="9751a-105">A maneira mais simples de criar um namespace é usar o código formato MOF (MOF) para criar o namespace dentro do diretório atual.</span><span class="sxs-lookup"><span data-stu-id="9751a-105">The simplest way of creating a namespace is to use Managed Object Format (MOF) code to create the namespace inside the current directory.</span></span> <span data-ttu-id="9751a-106">O diretório atual é definido quando você faz logon.</span><span class="sxs-lookup"><span data-stu-id="9751a-106">The current directory is defined when you log on.</span></span>

<span data-ttu-id="9751a-107">O procedimento a seguir descreve como criar um namespace filho usando o código MOF.</span><span class="sxs-lookup"><span data-stu-id="9751a-107">The following procedure describes how to create a child namespace using MOF code.</span></span>

<span data-ttu-id="9751a-108">**Para criar um namespace filho usando o código MOF**</span><span class="sxs-lookup"><span data-stu-id="9751a-108">**To create a child namespace using MOF code**</span></span>

1.  <span data-ttu-id="9751a-109">Crie uma instância da classe [**\_ \_ namespace**](--namespace.md) .</span><span class="sxs-lookup"><span data-stu-id="9751a-109">Create an instance of the [**\_\_Namespace**](--namespace.md) class.</span></span>

    <span data-ttu-id="9751a-110">O exemplo de código a seguir mostra como criar um namespace filho.</span><span class="sxs-lookup"><span data-stu-id="9751a-110">The following code example shows how to create a child namespace.</span></span>

    ``` syntax
    instance of __Namespace 
    {
        Name = "MyNamespace";
    };
    ```

2.  <span data-ttu-id="9751a-111">Se você quiser exigir que o usuário faça uma conexão criptografada com o namespace, use o qualificador **RequiresEncryption** .</span><span class="sxs-lookup"><span data-stu-id="9751a-111">If you want to require the user to make an encrypted connection to the namespace, use the **RequiresEncryption** qualifier.</span></span> <span data-ttu-id="9751a-112">Para obter mais informações, consulte [exigindo uma conexão criptografada para um namespace](requiring-an-encrypted-connection-to-a-namespace.md).</span><span class="sxs-lookup"><span data-stu-id="9751a-112">For more information, see [Requiring an Encrypted Connection to a Namespace](requiring-an-encrypted-connection-to-a-namespace.md).</span></span>

    <span data-ttu-id="9751a-113">O exemplo de código a seguir mostra como exigir uma conexão criptografada.</span><span class="sxs-lookup"><span data-stu-id="9751a-113">The following code example shows how to require an encrypted connection.</span></span>

    ``` syntax
    instance of __Namespace 
    {
        Name = "MyNamespace";
        [RequiresEncryption(TRUE)] 
        instance of __MyNamespace { };
    };
    ```

3.  <span data-ttu-id="9751a-114">Se você quiser definir um descritor de segurança no namespace em vez de usar a segurança de namespace padrão, use o qualificador **NamespaceSecuritySDDL** .</span><span class="sxs-lookup"><span data-stu-id="9751a-114">If you want to set a security descriptor on the namespace rather than using the default namespace security, use the **NamespaceSecuritySDDL** qualifier.</span></span> <span data-ttu-id="9751a-115">Para obter mais informações, consulte [definindo a segurança do namespace quando o namespace é criado](setting-namespace-security-when-the-namespace-is-created.md).</span><span class="sxs-lookup"><span data-stu-id="9751a-115">For more information, see [Setting Namespace Security When the Namespace is Created](setting-namespace-security-when-the-namespace-is-created.md).</span></span>

    <span data-ttu-id="9751a-116">O exemplo de código a seguir mostra como definir um descritor de segurança no namespace.</span><span class="sxs-lookup"><span data-stu-id="9751a-116">The following code example shows how to set a security descriptor on the namespace.</span></span>

    ``` syntax
    #pragma namespace("\\\\.\\root\\MyNamespace")

    [NamespaceSecuritySDDL ("O:AUG:AUD:(A;CI;0x00060033;;;WD)")]
    Instance of __Namespace
    {
      Name = "MyNamespace";
    };
    ```

4.  <span data-ttu-id="9751a-117">Compile e carregue a instância de [**\_ \_ namespace**](--namespace.md) usando o utilitário [Mofcomp](mofcomp.md) ou a interface [**IMofCompiler**](/windows/desktop/api/Wbemcli/nn-wbemcli-imofcompiler) .</span><span class="sxs-lookup"><span data-stu-id="9751a-117">Compile and load the [**\_\_Namespace**](--namespace.md) instance using the [mofcomp](mofcomp.md) utility or the [**IMofCompiler**](/windows/desktop/api/Wbemcli/nn-wbemcli-imofcompiler) interface.</span></span> <span data-ttu-id="9751a-118">Tanto o Mofcomp quanto a interface **IMofCompiler** carregam automaticamente o namespace no diretório atual.</span><span class="sxs-lookup"><span data-stu-id="9751a-118">Both mofcomp and the **IMofCompiler** interface automatically load the namespace into the current directory.</span></span> <span data-ttu-id="9751a-119">Para obter mais informações, consulte [compilando arquivos MOF](compiling-mof-files.md).</span><span class="sxs-lookup"><span data-stu-id="9751a-119">For more information, see [Compiling MOF Files](compiling-mof-files.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="9751a-120">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="9751a-120">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9751a-121">**Qualificadores WMI padrão**</span><span class="sxs-lookup"><span data-stu-id="9751a-121">**Standard WMI Qualifiers**</span></span>](standard-wmi-qualifiers.md)
</dt> </dl>

 

 



