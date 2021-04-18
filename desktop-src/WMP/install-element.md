---
title: Elemento de instalação
description: Observação Esta seção descreve a funcionalidade projetada para uso por lojas online. Não há suporte para o uso dessa funcionalidade fora do contexto de uma loja online. O elemento install especifica os valores usados pelo Windows Media Player para instalar uma loja online.
ms.assetid: 9a5e15ee-ec36-48d3-a1c2-bf20b6d2da48
keywords:
- Instalar o elemento Windows Media Player
topic_type:
- apiref
api_name:
- Install Element
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: bba56240651f789b45c18b006b16e5e07b10676e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105760255"
---
# <a name="install-element"></a><span data-ttu-id="09ccb-106">Elemento de instalação</span><span class="sxs-lookup"><span data-stu-id="09ccb-106">Install Element</span></span>

> [!Note]  
> <span data-ttu-id="09ccb-107">Esta seção descreve a funcionalidade projetada para uso por lojas online.</span><span class="sxs-lookup"><span data-stu-id="09ccb-107">This section describes functionality designed for use by online stores.</span></span> <span data-ttu-id="09ccb-108">Não há suporte para o uso dessa funcionalidade fora do contexto de uma loja online.</span><span class="sxs-lookup"><span data-stu-id="09ccb-108">Use of this functionality outside the context of an online store is not supported.</span></span>

 

<span data-ttu-id="09ccb-109">O elemento **install** especifica os valores usados pelo Windows Media Player para instalar uma loja online.</span><span class="sxs-lookup"><span data-stu-id="09ccb-109">The **Install** element specifies values used by Windows Media Player to install an online store.</span></span>

``` syntax
<Install
    EULAURL = "URL"
    CodeURL = "URL"
    PrivacyInfoURL = "URL"
    InstallApp = "filename"
    InstallData = "commandline"
    CatalogURL = "URL"
/>
```

## <a name="attributes"></a><span data-ttu-id="09ccb-110">Atributos</span><span class="sxs-lookup"><span data-stu-id="09ccb-110">Attributes</span></span>

<dl> <dt>

<span data-ttu-id="09ccb-111"><span id="EULAURL__required_"></span><span id="eulaurl__required_"></span><span id="EULAURL__REQUIRED_"></span>**EULAURL** (obrigatório)</span><span class="sxs-lookup"><span data-stu-id="09ccb-111"><span id="EULAURL__required_"></span><span id="eulaurl__required_"></span><span id="EULAURL__REQUIRED_"></span>**EULAURL** (required)</span></span>
</dt> <dd>

<span data-ttu-id="09ccb-112">URL totalmente qualificada para um arquivo com uma extensão de nome de arquivo. txt que o Windows Media Player usa para exibir um EULA (contrato de licença de usuário final).</span><span class="sxs-lookup"><span data-stu-id="09ccb-112">Fully qualified URL for a file with a .txt file name extension that Windows Media Player uses to display an End User License Agreement (EULA).</span></span> <span data-ttu-id="09ccb-113">Esse arquivo deve ser codificado no formato ANSI.</span><span class="sxs-lookup"><span data-stu-id="09ccb-113">This file must be encoded in ANSI format.</span></span>

</dd> <dt>

<span data-ttu-id="09ccb-114"><span id="CodeURL__required_"></span><span id="codeurl__required_"></span><span id="CODEURL__REQUIRED_"></span>**CodeURL** (obrigatório)</span><span class="sxs-lookup"><span data-stu-id="09ccb-114"><span id="CodeURL__required_"></span><span id="codeurl__required_"></span><span id="CODEURL__REQUIRED_"></span>**CodeURL** (required)</span></span>
</dt> <dd>

<span data-ttu-id="09ccb-115">URL totalmente qualificada para um pacote, com uma extensão de nome de arquivo. cab, que é usada para instalar a loja online.</span><span class="sxs-lookup"><span data-stu-id="09ccb-115">Fully qualified URL for a package, with a .cab file name extension, that is used to install the online store.</span></span> <span data-ttu-id="09ccb-116">O pacote e todos os módulos de código no pacote devem ser assinados.</span><span class="sxs-lookup"><span data-stu-id="09ccb-116">The package and all code modules in the package must be signed.</span></span> <span data-ttu-id="09ccb-117">Para obter informações sobre assinatura de código, consulte [introdução à assinatura de código](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms537361(v=vs.85)) na biblioteca MSDN.</span><span class="sxs-lookup"><span data-stu-id="09ccb-117">For information about code signing, see [Introduction to Code Signing](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms537361(v=vs.85)) in the MSDN Library.</span></span>

</dd> <dt>

<span data-ttu-id="09ccb-118"><span id="PrivacyInfoURL__required_"></span><span id="privacyinfourl__required_"></span><span id="PRIVACYINFOURL__REQUIRED_"></span>**PrivacyInfoURL** (obrigatório)</span><span class="sxs-lookup"><span data-stu-id="09ccb-118"><span id="PrivacyInfoURL__required_"></span><span id="privacyinfourl__required_"></span><span id="PRIVACYINFOURL__REQUIRED_"></span>**PrivacyInfoURL** (required)</span></span>
</dt> <dd>

<span data-ttu-id="09ccb-119">URL totalmente qualificada para uma página da Web que contém informações de política de privacidade para a loja online.</span><span class="sxs-lookup"><span data-stu-id="09ccb-119">Fully qualified URL for a webpage that contains privacy policy information for the online store.</span></span>

</dd> <dt>

<span data-ttu-id="09ccb-120"><span id="InstallApp__required_"></span><span id="installapp__required_"></span><span id="INSTALLAPP__REQUIRED_"></span>**InstallApp** (obrigatório)</span><span class="sxs-lookup"><span data-stu-id="09ccb-120"><span id="InstallApp__required_"></span><span id="installapp__required_"></span><span id="INSTALLAPP__REQUIRED_"></span>**InstallApp** (required)</span></span>
</dt> <dd>

<span data-ttu-id="09ccb-121">Nome do arquivo EXE ou INF a ser executado.</span><span class="sxs-lookup"><span data-stu-id="09ccb-121">Name of the EXE or INF file to run.</span></span> <span data-ttu-id="09ccb-122">Esse arquivo deve estar contido no arquivo CAB especificado pelo atributo **CodeURL** .</span><span class="sxs-lookup"><span data-stu-id="09ccb-122">This file must be contained in the CAB file specified by the **CodeURL** attribute.</span></span>

</dd> <dt>

<span data-ttu-id="09ccb-123"><span id="InstallData__optional_"></span><span id="installdata__optional_"></span><span id="INSTALLDATA__OPTIONAL_"></span>**InstallData** (opcional)</span><span class="sxs-lookup"><span data-stu-id="09ccb-123"><span id="InstallData__optional_"></span><span id="installdata__optional_"></span><span id="INSTALLDATA__OPTIONAL_"></span>**InstallData** (optional)</span></span>
</dt> <dd>

<span data-ttu-id="09ccb-124">Cadeia de caracteres de linha de comando que é passada para o aplicativo especificado pelo atributo **InstallApp** .</span><span class="sxs-lookup"><span data-stu-id="09ccb-124">Command-line string that is passed to the application specified by the **InstallApp** attribute.</span></span> <span data-ttu-id="09ccb-125">Esse atributo só é aplicável quando o valor de **InstallApp** especifica um executável.</span><span class="sxs-lookup"><span data-stu-id="09ccb-125">This attribute is only applicable when the value for **InstallApp** specifies an executable.</span></span>

</dd> <dt>

<span data-ttu-id="09ccb-126"><span id="CatalogURL__required_for_type_1__ignored_for_type_2_"></span><span id="catalogurl__required_for_type_1__ignored_for_type_2_"></span><span id="CATALOGURL__REQUIRED_FOR_TYPE_1__IGNORED_FOR_TYPE_2_"></span>**CatalogURL** (necessário para o tipo 1, ignorado para o tipo 2)</span><span class="sxs-lookup"><span data-stu-id="09ccb-126"><span id="CatalogURL__required_for_type_1__ignored_for_type_2_"></span><span id="catalogurl__required_for_type_1__ignored_for_type_2_"></span><span id="CATALOGURL__REQUIRED_FOR_TYPE_1__IGNORED_FOR_TYPE_2_"></span>**CatalogURL** (required for type 1, ignored for type 2)</span></span>
</dt> <dd>

<span data-ttu-id="09ccb-127">URL totalmente qualificada para o catálogo compilado do repositório online.</span><span class="sxs-lookup"><span data-stu-id="09ccb-127">Fully qualified URL for the online store's compiled catalog.</span></span>

</dd> </dl>

## <a name="parentchild-elements"></a><span data-ttu-id="09ccb-128">Elementos pai/filho</span><span class="sxs-lookup"><span data-stu-id="09ccb-128">Parent/Child Elements</span></span>



| <span data-ttu-id="09ccb-129">Hierarquia</span><span class="sxs-lookup"><span data-stu-id="09ccb-129">Hierarchy</span></span>       | <span data-ttu-id="09ccb-130">Elemento</span><span class="sxs-lookup"><span data-stu-id="09ccb-130">Element</span></span>         |
|-----------------|-----------------|
| <span data-ttu-id="09ccb-131">Elementos pai</span><span class="sxs-lookup"><span data-stu-id="09ccb-131">Parent elements</span></span> | <span data-ttu-id="09ccb-132">**ServiceInfo**</span><span class="sxs-lookup"><span data-stu-id="09ccb-132">**ServiceInfo**</span></span> |
| <span data-ttu-id="09ccb-133">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="09ccb-133">Child elements</span></span>  | <span data-ttu-id="09ccb-134">Nenhum</span><span class="sxs-lookup"><span data-stu-id="09ccb-134">None</span></span>            |



 

## <a name="remarks"></a><span data-ttu-id="09ccb-135">Comentários</span><span class="sxs-lookup"><span data-stu-id="09ccb-135">Remarks</span></span>

<span data-ttu-id="09ccb-136">Se algum dos atributos necessários estiver ausente ou não estiver disponível, a instalação do Windows Media Player não tentará baixar e instalar o código do provedor de loja online.</span><span class="sxs-lookup"><span data-stu-id="09ccb-136">If any of the required attributes are missing or not available, Windows Media Player setup will not attempt to download and install the online store provider code.</span></span> <span data-ttu-id="09ccb-137">A instalação configurará os valores padrão offline, conforme especificado no documento do **serviceInfo** .</span><span class="sxs-lookup"><span data-stu-id="09ccb-137">Setup will configure the offline default values as specified in the **ServiceInfo** document.</span></span> <span data-ttu-id="09ccb-138">O **serviceInfo** pode ser usado quando não estiver conectado à Internet, passando o nome do provedor padrão e as informações do **serviceInfo** como parâmetros de linha de comando.</span><span class="sxs-lookup"><span data-stu-id="09ccb-138">**ServiceInfo** can be used when not connected to the Internet by passing the default provider name and the **ServiceInfo** information as command-line parameters.</span></span> <span data-ttu-id="09ccb-139">Consulte [redistribuindo o software do Windows Media Player](redistributing-windows-media-player-software.md) para obter detalhes sobre as opções de linha de comando.</span><span class="sxs-lookup"><span data-stu-id="09ccb-139">See [Redistributing Windows Media Player Software](redistributing-windows-media-player-software.md) for details about command-line options.</span></span>

> [!Note]  
> <span data-ttu-id="09ccb-140">O uso deste elemento requer que você assine um contrato de redistribuição com a Microsoft.</span><span class="sxs-lookup"><span data-stu-id="09ccb-140">Use of this element requires that you sign a redistribution agreement with Microsoft.</span></span> <span data-ttu-id="09ccb-141">Entre em contato com seu representante de negócios para obter detalhes.</span><span class="sxs-lookup"><span data-stu-id="09ccb-141">Contact your business representative for details.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="09ccb-142">Requisitos</span><span class="sxs-lookup"><span data-stu-id="09ccb-142">Requirements</span></span>



| <span data-ttu-id="09ccb-143">Requisito</span><span class="sxs-lookup"><span data-stu-id="09ccb-143">Requirement</span></span> | <span data-ttu-id="09ccb-144">Valor</span><span class="sxs-lookup"><span data-stu-id="09ccb-144">Value</span></span> |
|--------------------|----------------------------------------------|
| <span data-ttu-id="09ccb-145">Versão</span><span class="sxs-lookup"><span data-stu-id="09ccb-145">Version</span></span><br/> | <span data-ttu-id="09ccb-146">Windows Media Player 10 ou posterior.</span><span class="sxs-lookup"><span data-stu-id="09ccb-146">Windows Media Player 10 or later.</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="09ccb-147">Confira também</span><span class="sxs-lookup"><span data-stu-id="09ccb-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="09ccb-148">**Documento de informações de exemplo para uma loja online tipo 1**</span><span class="sxs-lookup"><span data-stu-id="09ccb-148">**Example ServiceInfo Document for a Type 1 Online Store**</span></span>](example-serviceinfo-document-for-a-type-1-online-store.md)
</dt> <dt>

[<span data-ttu-id="09ccb-149">**Documento de informações de exemplo para uma loja online tipo 2**</span><span class="sxs-lookup"><span data-stu-id="09ccb-149">**Example ServiceInfo Document for a Type 2 Online Store**</span></span>](example-serviceinfo-document-for-a-type-2-online-store.md)
</dt> <dt>

[<span data-ttu-id="09ccb-150">**Documento do serviceInfo**</span><span class="sxs-lookup"><span data-stu-id="09ccb-150">**ServiceInfo Document**</span></span>](serviceinfo-document.md)
</dt> </dl>

 

