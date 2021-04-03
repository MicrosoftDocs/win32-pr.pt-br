---
title: Programando ADSI com Java/COM
description: Usando a máquina virtual da Microsoft para Java (Microsoft VM) e o compilador do Microsoft Java, você tem acesso a todos os recursos ADSI expostos por meio de qualquer componente COM do ADSI, de um aplicativo Java/COM.
ms.assetid: eda516b6-0f89-464f-a9d2-9bb4ca70fda5
ms.tgt_platform: multiple
keywords:
- Programando ADSI com o AD do Java/COM
- ADSI ADSI, usando a programação Java/COM para
- ADSI ADSI, código de exemplo Java
- ADSI ADSI, exemplo de código Java, associando a um objeto ADSI e invocando métodos nesse objeto
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b6899804208f9899823f266bc941bcf3c2dec372
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103822193"
---
# <a name="programming-adsi-with-javacom"></a><span data-ttu-id="ecc2b-107">Programando ADSI com Java/COM</span><span class="sxs-lookup"><span data-stu-id="ecc2b-107">Programming ADSI with Java/COM</span></span>

<span data-ttu-id="ecc2b-108">Usando a máquina virtual da Microsoft para Java (Microsoft VM) e o compilador do Microsoft Java, você tem acesso a todos os recursos ADSI expostos por meio de qualquer componente COM do ADSI, de um aplicativo Java/COM.</span><span class="sxs-lookup"><span data-stu-id="ecc2b-108">Using the Microsoft virtual machine for Java (Microsoft VM) and Microsoft Java Compiler, you have access to all the ADSI features exposed through any ADSI COM components, from a Java/COM application.</span></span> <span data-ttu-id="ecc2b-109">O exemplo de código Java a seguir mostra os elementos necessários para associar a um objeto ADSI e invocar métodos nesse objeto.</span><span class="sxs-lookup"><span data-stu-id="ecc2b-109">The following Java code example shows the elements necessary to bind to an ADSI object and invoke methods on that object.</span></span> <span data-ttu-id="ecc2b-110">As funções de API ADSI necessárias e os métodos de objeto são expostos por meio de Activeds.dll.</span><span class="sxs-lookup"><span data-stu-id="ecc2b-110">The required ADSI API functions and object methods are exposed through Activeds.dll.</span></span>


```C++
import activeds.*;       // ADSI COM Wrapper classes
import com.ms.com.*;     // to use _Guid data type in COM.

public Class SimpleADSI 
{
    IADs obj;
    String path = "WinNT://domain/machine,computer";
    _Guid riid = IADs.iid;
    public static void main(String args[]) 
    {
        try 
        {
            obj = (IADs)ADsGetObject(path, riid);
            System.out.println( "Object name:  " + obj.getName() );
            System.out.println( "      class:  " + obj.getSchema() );
            System.out.println( "    ADsPath:  " + obj.getADsPath() );
            System.out.println( "     parent:  " + obj.getParent() );
        }
        catch (Exception e) 
        {
            System.out.println( "SimpleADSI Error: " + e.toString() );
        }
    }

    /** @dll.import("activeds", ole) */
    private static native IUnknown ADsGetObject(String path, _Guid riid);
}
```



<span data-ttu-id="ecc2b-111">O argumento na primeira instrução **Import** refere-se às classes de wrapper Java empacotadas no Activeds.dll.</span><span class="sxs-lookup"><span data-stu-id="ecc2b-111">The argument in the first **import** statement refers to Java Wrapper classes packaged in Activeds.dll.</span></span> <span data-ttu-id="ecc2b-112">Use o Visual J++ para criar as classes de wrapper e incluí-las em seu projeto, seguindo o procedimento abaixo.</span><span class="sxs-lookup"><span data-stu-id="ecc2b-112">Use Visual J++ to create the wrapper classes and include them in your project, following the procedure below.</span></span>

<span data-ttu-id="ecc2b-113">**Para criar classes de wrapper e incluí-las em seu projeto**</span><span class="sxs-lookup"><span data-stu-id="ecc2b-113">**To create wrapper classes and include them in your project**</span></span>

1.  <span data-ttu-id="ecc2b-114">Em um projeto do Visual J++, selecione **Adicionar wrapper com...** no menu do **projeto** .</span><span class="sxs-lookup"><span data-stu-id="ecc2b-114">In a Visual J++ project, select **Add Com Wrapper...** from the **Project** menu.</span></span>
2.  <span data-ttu-id="ecc2b-115">Selecione "biblioteca de tipos do Active DS" nos **componentes instalados:** na caixa de diálogo wrappers com.</span><span class="sxs-lookup"><span data-stu-id="ecc2b-115">Select "Active DS Type Library" from the **Installed Components:** from the COM Wrappers dialog.</span></span> <span data-ttu-id="ecc2b-116">Se a biblioteca de tipos não for mostrada na caixa de listagem, clique no botão **procurar...** , navegue até o diretório onde activeds. tlb está armazenado e, em seguida, selecione a biblioteca de tipos.</span><span class="sxs-lookup"><span data-stu-id="ecc2b-116">If the type library is not shown in the list box, click the **Browse...** button, navigate to the directory where Activeds.tlb is stored, and then select the type library.</span></span>

<span data-ttu-id="ecc2b-117">O Visual J++ cria o pacote activeds para as classes de wrapper Java e inclui o pacote no caminho padrão do projeto.</span><span class="sxs-lookup"><span data-stu-id="ecc2b-117">Visual J++ creates the activeds package for the Java Wrapper classes and include the package into the project's default path.</span></span> <span data-ttu-id="ecc2b-118">Para obter mais informações, consulte o pacote activeds no painel **explorar do projeto** na janela do Visual J++.</span><span class="sxs-lookup"><span data-stu-id="ecc2b-118">For more information, see the activeds package in the **Project Explore** pane on the Visual J++ window.</span></span>

<span data-ttu-id="ecc2b-119">Para obter um objeto ADSI que não pode ser Cocriado, use uma das funções de API ADSI expostas, por exemplo, [**ADsGetObject**](/windows/desktop/api/Adshlp/nf-adshlp-adsgetobject) ou [**ADsOpenObject**](/windows/desktop/api/Adshlp/nf-adshlp-adsopenobject), que também são empacotadas em Activeds.dll.</span><span class="sxs-lookup"><span data-stu-id="ecc2b-119">To get an ADSI object that cannot be cocreated, use one of the exposed ADSI API functions, for example, [**ADsGetObject**](/windows/desktop/api/Adshlp/nf-adshlp-adsgetobject) or [**ADsOpenObject**](/windows/desktop/api/Adshlp/nf-adshlp-adsopenobject), which are also packaged in Activeds.dll.</span></span> <span data-ttu-id="ecc2b-120">O Microsoft J/Direct fornece acesso a essas e a outras APIs nativas.</span><span class="sxs-lookup"><span data-stu-id="ecc2b-120">Microsoft J/Direct provides access to these and other native APIs.</span></span> <span data-ttu-id="ecc2b-121">Isso é ilustrado pelas duas últimas linhas do exemplo de código acima.</span><span class="sxs-lookup"><span data-stu-id="ecc2b-121">This is illustrated by the last two lines of the code example, above.</span></span>

<span data-ttu-id="ecc2b-122">Ao compilar, verifique se a extensão de idioma da Microsoft está habilitada.</span><span class="sxs-lookup"><span data-stu-id="ecc2b-122">When compiling, ensure that Microsoft Language Extension is enabled.</span></span> <span data-ttu-id="ecc2b-123">Para fazer isso, selecione **<project> Propriedades...** no menu **projeto** na janela do projeto do Visual J++.</span><span class="sxs-lookup"><span data-stu-id="ecc2b-123">To do this, select **<project> Properties...** from the **Project** menu in the Visual J++ project window.</span></span> <span data-ttu-id="ecc2b-124">Em seguida, clique na guia **Compilar** na caixa de diálogo **<project> Propriedades** .</span><span class="sxs-lookup"><span data-stu-id="ecc2b-124">Then, click the **Compile** tab in the **<project> Properties** dialog.</span></span> <span data-ttu-id="ecc2b-125">Desmarque a caixa de seleção **desabilitar extensões de idioma da Microsoft** .</span><span class="sxs-lookup"><span data-stu-id="ecc2b-125">Clear the **Disable Microsoft Language Extensions** check box.</span></span> <span data-ttu-id="ecc2b-126">Se estiver compilando na linha de comando, use a opção "/x-", por exemplo:</span><span class="sxs-lookup"><span data-stu-id="ecc2b-126">If compiling from the command line, use "/x-" switch, for example:</span></span>

<span data-ttu-id="ecc2b-127">**JVC/x-SimpleADSI. java**</span><span class="sxs-lookup"><span data-stu-id="ecc2b-127">**jvc /x- SimpleADSI.java**</span></span>

<span data-ttu-id="ecc2b-128">Por fim, para que a máquina virtual carregue o componente COM, a DLL (biblioteca de vínculo dinâmico) deve estar visível no caminho do sistema.</span><span class="sxs-lookup"><span data-stu-id="ecc2b-128">Finally, in order for the virtual machine to load the COM component, the dynamic-link library (DLL) must be visible on the system path.</span></span> <span data-ttu-id="ecc2b-129">Se um erro "Java. lang. UnsatisfiedLinkError" for retornado, defina o caminho para incluir o caminho que contém a DLL necessária.</span><span class="sxs-lookup"><span data-stu-id="ecc2b-129">If a "java.lang.UnsatisfiedLinkError" error is returned, set the PATH to include the path that contains the required DLL.</span></span> <span data-ttu-id="ecc2b-130">Por exemplo, se Activeds.dll tiver sido instalado em c: \\ ADSI \\ lib, emita o seguinte comando na linha de comando:</span><span class="sxs-lookup"><span data-stu-id="ecc2b-130">For example, if Activeds.dll has been installed in c:\\adsi\\lib, issue the following command from the command line:</span></span>

<span data-ttu-id="ecc2b-131">**Definir caminho =% PATH%; c: \\ ADSI \\ lib**</span><span class="sxs-lookup"><span data-stu-id="ecc2b-131">**set PATH = %PATH%; c:\\adsi\\lib**</span></span>

 

 




