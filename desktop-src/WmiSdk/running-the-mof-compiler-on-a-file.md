---
description: 'Você tem duas opções ao compilar um arquivo MOF: usando o utilitário de linha de comando ou usando uma interface programática.'
ms.assetid: 1760f1bd-7027-4201-97a2-ca902f945b52
ms.tgt_platform: multiple
title: Executando o compilador MOF em um arquivo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 77f62834944e995c3e7f3763c460d72f9f70aa66
ms.sourcegitcommit: 7eadd92b1da5eb4eab7d516a5a768e7f7fc02d4c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/16/2021
ms.locfileid: "112230233"
---
# <a name="running-the-mof-compiler-on-a-file"></a><span data-ttu-id="2c45e-103">Executando o compilador MOF em um arquivo</span><span class="sxs-lookup"><span data-stu-id="2c45e-103">Running the MOF Compiler on a File</span></span>

<span data-ttu-id="2c45e-104">Você tem duas opções ao compilar um arquivo MOF: usando o utilitário de linha de comando ou usando uma interface programática.</span><span class="sxs-lookup"><span data-stu-id="2c45e-104">You have two choices when compiling a MOF file: using the command-line utility or using a programmatic interface.</span></span>

<span data-ttu-id="2c45e-105">Até que você execute o compilador MOF, [**Mofcomp.exe**](mofcomp.md), um provedor não está registrado com o WMI e as classes criadas no arquivo MOF não estão disponíveis no [*repositório WMI*](gloss-w.md).</span><span class="sxs-lookup"><span data-stu-id="2c45e-105">Until you run the MOF compiler, [**Mofcomp.exe**](mofcomp.md), a provider is not registered with WMI and the classes it created in the MOF file are not available in the [*WMI repository*](gloss-w.md).</span></span> <span data-ttu-id="2c45e-106">O procedimento a seguir descreve como compilar um arquivo MOF.</span><span class="sxs-lookup"><span data-stu-id="2c45e-106">The following procedure describes how to compile a MOF file.</span></span>

<span data-ttu-id="2c45e-107">**Para executar o compilador MOF em um arquivo da linha de comando**</span><span class="sxs-lookup"><span data-stu-id="2c45e-107">**To run the MOF compiler on a file from the command line**</span></span>

1.  <span data-ttu-id="2c45e-108">Chame o compilador MOF na linha de comando, usando a sintaxe a seguir.</span><span class="sxs-lookup"><span data-stu-id="2c45e-108">Call the MOF compiler from the command line, using the following syntax.</span></span>

    <span data-ttu-id="2c45e-109">**Mofcomp** _MOFfile_**. mof**</span><span class="sxs-lookup"><span data-stu-id="2c45e-109">**mofcomp** _MOFfile_**.mof**</span></span>

    <span data-ttu-id="2c45e-110">O compilador MOF dá suporte a uma variedade de opções para controlar situações de processamento especiais.</span><span class="sxs-lookup"><span data-stu-id="2c45e-110">The MOF compiler supports a variety of switches to control special processing situations.</span></span> <span data-ttu-id="2c45e-111">Todas as opções são opcionais e qualquer combinação de opções é permitida.</span><span class="sxs-lookup"><span data-stu-id="2c45e-111">All of the switches are optional, and any combination of switches is allowed.</span></span> <span data-ttu-id="2c45e-112">No entanto, não faz sentido usar alguns dos comutadores em combinação com outros.</span><span class="sxs-lookup"><span data-stu-id="2c45e-112">However, it does not make sense to use some of the switches in combination with others.</span></span> <span data-ttu-id="2c45e-113">Por exemplo, para combinar as opções **-Class: UpdateOnly** e **-Class: createonly** , os resultados do compilador não executam nenhuma ação.</span><span class="sxs-lookup"><span data-stu-id="2c45e-113">For example, to combine the **-class:updateonly** and **-class:createonly** switches results in the compiler not performing any action.</span></span>

    <span data-ttu-id="2c45e-114">Por padrão, o Mofcomp.exe armazena as classes compiladas no \\ namespace WMI padrão raiz.</span><span class="sxs-lookup"><span data-stu-id="2c45e-114">By default, Mofcomp.exe stores the compiled classes in the root\\default WMI namespace.</span></span> <span data-ttu-id="2c45e-115">Observe que o namespace padrão para Mofcomp.exe não é o mesmo que o namespace padrão para scripts.</span><span class="sxs-lookup"><span data-stu-id="2c45e-115">Note that the default namespace for Mofcomp.exe is not the same as the default namespace for scripting.</span></span> <span data-ttu-id="2c45e-116">O namespace padrão para scripts é especificado no controle WMI na guia Avançado. Para obter mais informações, consulte [definindo a segurança do namespace com o controle WMI](setting-namespace-security-with-the-wmi-control.md).</span><span class="sxs-lookup"><span data-stu-id="2c45e-116">The default namespace for scripting is specified in the WMI Control on the Advanced tab. For more information, see [Setting Namespace Security with the WMI Control](setting-namespace-security-with-the-wmi-control.md).</span></span>

    <span data-ttu-id="2c45e-117">Você pode alterar o namespace que recebe as classes de duas maneiras.</span><span class="sxs-lookup"><span data-stu-id="2c45e-117">You can change the namespace that receives the classes in two ways.</span></span>

    1.  <span data-ttu-id="2c45e-118">Use a opção **-N** para o comando **Mofcomp** .</span><span class="sxs-lookup"><span data-stu-id="2c45e-118">Use the **-N** switch for the **mofcomp** command.</span></span>
    2.  <span data-ttu-id="2c45e-119">Insira o namespace de pragma do comando de pré-processador \# [](pragma-namespace.md) no arquivo MOF.</span><span class="sxs-lookup"><span data-stu-id="2c45e-119">Insert the preprocessor command \#[**pragma namespace**](pragma-namespace.md) in the MOF file.</span></span>

2.  <span data-ttu-id="2c45e-120">Opcionalmente, você pode compilar um arquivo MOF programaticamente.</span><span class="sxs-lookup"><span data-stu-id="2c45e-120">Optionally, you can compile a MOF file programmatically.</span></span> <span data-ttu-id="2c45e-121">Para obter mais informações, consulte [**IMofCompiler**](/windows/desktop/api/Wbemcli/nn-wbemcli-imofcompiler).</span><span class="sxs-lookup"><span data-stu-id="2c45e-121">For more information, see [**IMofCompiler**](/windows/desktop/api/Wbemcli/nn-wbemcli-imofcompiler).</span></span>

## <a name="related-topics"></a><span data-ttu-id="2c45e-122">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="2c45e-122">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2c45e-123">Compilando arquivos MOF</span><span class="sxs-lookup"><span data-stu-id="2c45e-123">Compiling MOF Files</span></span>](compiling-mof-files.md)
</dt> <dt>

[<span data-ttu-id="2c45e-124">**Mofcomp**</span><span class="sxs-lookup"><span data-stu-id="2c45e-124">**mofcomp**</span></span>](mofcomp.md)
</dt> <dt>

[<span data-ttu-id="2c45e-125">Comandos de pré-processador</span><span class="sxs-lookup"><span data-stu-id="2c45e-125">Preprocessor Commands</span></span>](preprocessor-commands.md)
</dt> </dl>

 

 



