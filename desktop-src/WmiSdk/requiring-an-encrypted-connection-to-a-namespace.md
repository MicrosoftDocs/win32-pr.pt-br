---
description: Você pode exigir que os scripts e aplicativos de cliente estabeleçam uma conexão criptografada para autenticação adicionando o qualificador RequiresEncryption ao arquivo MOF (formato MOF). MOF que cria o namespace.
ms.assetid: 07b225a2-3834-4879-beae-f5b9180d112f
ms.tgt_platform: multiple
title: Exigindo uma conexão criptografada para um namespace
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e42415c0f714f99a51d6a1a0ee1a0b22f398b1b7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105763434"
---
# <a name="requiring-an-encrypted-connection-to-a-namespace"></a><span data-ttu-id="960bb-103">Exigindo uma conexão criptografada para um namespace</span><span class="sxs-lookup"><span data-stu-id="960bb-103">Requiring an Encrypted Connection to a Namespace</span></span>

<span data-ttu-id="960bb-104">Você pode exigir que os scripts e aplicativos de cliente estabeleçam uma conexão criptografada para autenticação adicionando o qualificador **RequiresEncryption** ao arquivo mof (formato MOF). MOF que cria o namespace.</span><span class="sxs-lookup"><span data-stu-id="960bb-104">You can require that client scripts and applications establish an encrypted connection for authentication by adding the **RequiresEncryption** qualifier to the Managed Object Format (MOF) .mof file that creates the namespace.</span></span>


<span data-ttu-id="960bb-105">Uma conexão criptografada com um namespace WMI especifica a **privacidade do PCT do \_ nível de \_ autenticação RPC \_ \_ \_ C** (ou **PktPrivacy** em um script) para autenticação.</span><span class="sxs-lookup"><span data-stu-id="960bb-105">An encrypted connection to a WMI namespace specifies **RPC\_C\_AUTHN\_LEVEL\_PKT\_PRIVACY** (or **PktPrivacy** in a script) for authentication.</span></span> <span data-ttu-id="960bb-106">O qualificador **RequiresEncryption** faz com que o WMI rejeite quaisquer solicitações de dados de entrada, a menos que elas usem explicitamente a autenticação criptografada.</span><span class="sxs-lookup"><span data-stu-id="960bb-106">The **RequiresEncryption** qualifier causes WMI to reject any incoming data requests unless they explicitly use encrypted authentication.</span></span> <span data-ttu-id="960bb-107">Para obter mais informações, consulte [definindo o nível de segurança do processo padrão usando o VBScript](setting-the-default-process-security-level-using-vbscript.md) ou definindo a [autenticação usando C++](setting-authentication-using-c-.md).</span><span class="sxs-lookup"><span data-stu-id="960bb-107">For more information, see [Setting the Default Process Security Level Using VBScript](setting-the-default-process-security-level-using-vbscript.md) or [Setting Authentication Using C++](setting-authentication-using-c-.md).</span></span>

<span data-ttu-id="960bb-108">Você também pode modificar um namespace existente adicionando esse atributo e, em seguida, compilando o arquivo MOF novamente.</span><span class="sxs-lookup"><span data-stu-id="960bb-108">You can also modify an existing namespace by adding this attribute and then compile the MOF file again.</span></span> <span data-ttu-id="960bb-109">**RequiresEncryption** é usado no [*MOF*](gloss-m.md) com a instrução de pré-processador do [namespace pragma](pragma-namespace.md) .</span><span class="sxs-lookup"><span data-stu-id="960bb-109">**RequiresEncryption** is used in [*MOF*](gloss-m.md) with the [pragma namespace](pragma-namespace.md) preprocessor instruction.</span></span>

<span data-ttu-id="960bb-110">O procedimento a seguir define o namespace para exigir uma conexão criptografada.</span><span class="sxs-lookup"><span data-stu-id="960bb-110">The following procedure sets the namespace to require an encrypted connection.</span></span>

<span data-ttu-id="960bb-111">**Para definir a criptografia necessária**</span><span class="sxs-lookup"><span data-stu-id="960bb-111">**To set required encryption**</span></span>

1.  <span data-ttu-id="960bb-112">Crie um arquivo de formato MOF (MOF) ou modifique o arquivo MOF existente que define o namespace.</span><span class="sxs-lookup"><span data-stu-id="960bb-112">Create a Managed Object Format (MOF) file or modify your existing MOF file that defines the namespace.</span></span>

    <span data-ttu-id="960bb-113">O exemplo de código a seguir mostra o namespace que será modificado como *root \\ MyNamespace* e o arquivo é chamado *MyNamespace \_ Security. mof*.</span><span class="sxs-lookup"><span data-stu-id="960bb-113">The following code example shows the namespace that will be modified is *root\\MyNamespace* and the file is named *MyNamespace\_security.mof*.</span></span> <span data-ttu-id="960bb-114">**RequiresEncryption** tem um tipo de dados booliano para que ele deva ser definido como **true** ou **false**.</span><span class="sxs-lookup"><span data-stu-id="960bb-114">**RequiresEncryption** has a Boolean datatype so it must be set to **True** or **False**.</span></span>

    ```mof
    #pragma namespace("\\\\.\\Root\\MyNamespace") 

    [RequiresEncryption(TRUE)] 
    instance of __systemSecurity { };
    ```

    

2.  <span data-ttu-id="960bb-115">Execute [**mofcomp.exe**](mofcomp.md) para compilar o arquivo MOF.</span><span class="sxs-lookup"><span data-stu-id="960bb-115">Run [**mofcomp.exe**](mofcomp.md) to compile the MOF file.</span></span>

    <span data-ttu-id="960bb-116">**c: \\ Mofcomp MyNamespace \_ Security. mof**</span><span class="sxs-lookup"><span data-stu-id="960bb-116">**c:\\mofcomp MyNamespace\_security.mof**</span></span>

    <span data-ttu-id="960bb-117">Em C++, use os métodos [**IMoFCompiler**](/windows/desktop/api/Wbemcli/nn-wbemcli-imofcompiler) .</span><span class="sxs-lookup"><span data-stu-id="960bb-117">In C++, use the [**IMoFCompiler**](/windows/desktop/api/Wbemcli/nn-wbemcli-imofcompiler) methods.</span></span>

<span data-ttu-id="960bb-118">O WMI rejeita um cliente que usa o nível de autenticação padrão porque o DCOM negocia a segurança para o nível exigido pelo processo SVCHOST no qual o serviço WMI está em execução.</span><span class="sxs-lookup"><span data-stu-id="960bb-118">WMI rejects a client that uses the default authentication level because DCOM negotiates the security to the level required by the SVCHOST process in which the WMI service is running.</span></span> <span data-ttu-id="960bb-119">Para obter mais informações sobre hosts de serviço, consulte [provedor de hospedagem e segurança](provider-hosting-and-security.md).</span><span class="sxs-lookup"><span data-stu-id="960bb-119">For more information about service hosts, see [Provider Hosting and Security](provider-hosting-and-security.md).</span></span> <span data-ttu-id="960bb-120">Para obter mais informações sobre como configurar níveis de autenticação ao se conectar a namespaces do WMI, consulte [definindo o nível de segurança do processo padrão usando c++](setting-the-default-process-security-level-using-c-.md), [definindo a autenticação usando c++](setting-authentication-using-c-.md)ou [definindo o nível de segurança do processo padrão usando o VBScript](setting-the-default-process-security-level-using-vbscript.md).</span><span class="sxs-lookup"><span data-stu-id="960bb-120">For more information about setting authentication levels when connecting to WMI namespaces, see [Setting the Default Process Security Level Using C++](setting-the-default-process-security-level-using-c-.md), [Setting Authentication Using C++](setting-authentication-using-c-.md), or [Setting the Default Process Security Level Using VBScript](setting-the-default-process-security-level-using-vbscript.md).</span></span>

<span data-ttu-id="960bb-121">Ao retornar dados em uma conexão de retorno de chamada assíncrona, o WMI retorna uma mensagem de acesso negado ao computador solicitante.</span><span class="sxs-lookup"><span data-stu-id="960bb-121">When returning data on an asynchronous callback connection, WMI returns an access denied message to the requesting computer.</span></span> <span data-ttu-id="960bb-122">O WMI também faz uma entrada de log no log de eventos NT do computador com o namespace criptografado informando que não é possível estabelecer uma conexão segura com o cliente.</span><span class="sxs-lookup"><span data-stu-id="960bb-122">WMI also makes a log entry in the NT Event Log of the computer with the encrypted namespace stating that a secure connection cannot be established to the client.</span></span>

<span data-ttu-id="960bb-123">A partir do Windows Vista, o arquivo WbemCore. log não existe mais.</span><span class="sxs-lookup"><span data-stu-id="960bb-123">Starting with Windows Vista, the WbemCore.log file no longer exists.</span></span> <span data-ttu-id="960bb-124">Você pode verificar o log de eventos NT para entradas que indicam solicitações de dados de entrada rejeitadas para namespaces que exigem Criptografia.</span><span class="sxs-lookup"><span data-stu-id="960bb-124">You can check the NT Event Log for entries indicating rejected inbound data requests to namespaces that require encryption.</span></span>

## <a name="related-topics"></a><span data-ttu-id="960bb-125">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="960bb-125">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="960bb-126">Configurando descritores de segurança namepace</span><span class="sxs-lookup"><span data-stu-id="960bb-126">Setting Namepace Security Descriptors</span></span>](setting-namespace-security-descriptors.md)
</dt> <dt>

[<span data-ttu-id="960bb-127">**WbemAuthenticationLevelEnum**</span><span class="sxs-lookup"><span data-stu-id="960bb-127">**WbemAuthenticationLevelEnum**</span></span>](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemauthenticationlevelenum)
</dt> <dt>

[<span data-ttu-id="960bb-128">Protegendo uma conexão WMI remota</span><span class="sxs-lookup"><span data-stu-id="960bb-128">Securing a Remote WMI Connection</span></span>](securing-a-remote-wmi-connection.md)
</dt> </dl>

 

 



