---
title: Extensões de unidade de dados
description: Extensões de unidade de dados
ms.assetid: f95de189-0449-4b88-aba3-7b19f385c8fe
keywords:
- SDK do Windows Media Format, extensões de unidade de dados
- ASF (Advanced Systems Format), extensões de unidade de dados
- ASF (formato de sistemas avançados), extensões de unidade de dados
- SDK do Windows Media Format, sistemas de extensão de carga
- ASF (Advanced Systems Format), sistemas de extensão de carga
- ASF (formato de sistemas avançados), sistemas de extensão de carga
- extensões de unidade de dados, sobre
- extensões de unidade de carga
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3c8ed5c9db82d0002648148ca14bd7f94baa9029
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/19/2020
ms.locfileid: "103640145"
---
# <a name="data-unit-extensions"></a><span data-ttu-id="0e68b-111">Extensões de unidade de dados</span><span class="sxs-lookup"><span data-stu-id="0e68b-111">Data Unit Extensions</span></span>

<span data-ttu-id="0e68b-112">O SDK do Windows Media Format permite que você complemente dados em exemplos com *extensões de unidade de dados*, também chamadas de sistemas de extensão de carga.</span><span class="sxs-lookup"><span data-stu-id="0e68b-112">The Windows Media Format SDK enables you to supplement data in samples with *data unit extensions*, also called payload extension systems.</span></span> <span data-ttu-id="0e68b-113">Esta documentação usa o termo "extensões de unidade de dados" para permanecer consistente com nomes de métodos como [**AddDataUnitExtension**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmstreamconfig2-adddataunitextension).</span><span class="sxs-lookup"><span data-stu-id="0e68b-113">This documentation uses the term "data unit extensions" in order to remain consistent with method names such as [**AddDataUnitExtension**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmstreamconfig2-adddataunitextension).</span></span> <span data-ttu-id="0e68b-114">Uma extensão de unidade de dados é um par de nome/valor que é anexado ao exemplo na seção de dados do arquivo.</span><span class="sxs-lookup"><span data-stu-id="0e68b-114">A data unit extension is a name/value pair that is attached to the sample in the data section of the file.</span></span> <span data-ttu-id="0e68b-115">Você pode acessar os dados estendidos usando métodos do objeto buffer quando o exemplo é recuperado pelo leitor.</span><span class="sxs-lookup"><span data-stu-id="0e68b-115">You can access the extended data using methods of the buffer object when the sample is retrieved by the reader.</span></span>

<span data-ttu-id="0e68b-116">Você pode criar extensões de unidade de dados para suas próprias especificações, mas vários tipos são predefinidos e suportados pelos objetos desse SDK.</span><span class="sxs-lookup"><span data-stu-id="0e68b-116">You can create data unit extensions to your own specifications, but several types are predefined and supported by the objects of this SDK.</span></span> <span data-ttu-id="0e68b-117">Essas extensões padrão são usadas para fornecer dados adicionais para nomes de arquivo (em fluxos de script e Web), dados de código de tempo SMPTE, taxa de proporção de pixel não quadrado, duração e tipo de entrelaçamento.</span><span class="sxs-lookup"><span data-stu-id="0e68b-117">These standard extensions are used to provide additional data for file names (in script and Web streams), SMPTE time code data, non-square pixel aspect ratio, duration, and type of interlacing.</span></span>

<span data-ttu-id="0e68b-118">Para usar extensões de unidade de dados, você deve configurar o fluxo para aceitá-los e, em seguida, adicionar extensões a cada exemplo para esse fluxo.</span><span class="sxs-lookup"><span data-stu-id="0e68b-118">To use data unit extensions, you must configure the stream to accept them, and then add extensions to each sample for that stream.</span></span>

## <a name="related-topics"></a><span data-ttu-id="0e68b-119">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="0e68b-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0e68b-120">**Recursos de arquivo ASF**</span><span class="sxs-lookup"><span data-stu-id="0e68b-120">**ASF File Features**</span></span>](asf-file-features.md)
</dt> <dt>

[<span data-ttu-id="0e68b-121">**Configurar extensões de unidade de dados**</span><span class="sxs-lookup"><span data-stu-id="0e68b-121">**Configuring Data Unit Extensions**</span></span>](configuring-data-unit-extensions.md)
</dt> <dt>

[<span data-ttu-id="0e68b-122">**Definindo extensões de unidade de dados**</span><span class="sxs-lookup"><span data-stu-id="0e68b-122">**Setting Data Unit Extensions**</span></span>](setting-data-unit-extensions.md)
</dt> </dl>

 

 




