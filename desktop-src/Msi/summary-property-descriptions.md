---
description: As propriedades de resumo para pacotes de instalação, transformações e patches são descritos nas tabelas a seguir.
ms.assetid: b44b24b7-7fc4-4c3c-9d10-7e2f3c43cf36
title: Descrições de propriedades de resumo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 41addb58571b6d18e1cccc4a34c3026f3d0544cf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105782324"
---
# <a name="summary-property-descriptions"></a><span data-ttu-id="b165a-103">Descrições de propriedades de resumo</span><span class="sxs-lookup"><span data-stu-id="b165a-103">Summary Property Descriptions</span></span>

<span data-ttu-id="b165a-104">As propriedades de resumo para pacotes de instalação, transformações e patches são descritos nas tabelas a seguir.</span><span class="sxs-lookup"><span data-stu-id="b165a-104">Summary properties for installation packages, transforms, and patches are described in the following tables.</span></span> <span data-ttu-id="b165a-105">Observe que o significado de uma determinada propriedade de resumo pode ser diferente dependendo se o banco de dados pertence a um pacote de instalação, transformação ou pacote de patch.</span><span class="sxs-lookup"><span data-stu-id="b165a-105">Note that the meaning of a particular summary property can be different depending on whether the database belongs to an installation package, transform, or patch package.</span></span> <span data-ttu-id="b165a-106">Para obter mais informações sobre as IDs de propriedade, PIDs e tipos, consulte [Summary Information Stream Property Set](summary-information-stream-property-set.md).</span><span class="sxs-lookup"><span data-stu-id="b165a-106">For more information about the property IDs, PIDs, and types, see [Summary Information Stream Property Set](summary-information-stream-property-set.md).</span></span>

## <a name="installation-packages"></a><span data-ttu-id="b165a-107">Pacotes de instalação</span><span class="sxs-lookup"><span data-stu-id="b165a-107">Installation Packages</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="b165a-108">Propriedade Summary</span><span class="sxs-lookup"><span data-stu-id="b165a-108">Summary property</span></span></th>
<th><span data-ttu-id="b165a-109">Significado dessa propriedade em um banco de dados de instalação</span><span class="sxs-lookup"><span data-stu-id="b165a-109">Meaning of this property in an Installation database</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="b165a-110"><a href="title-summary.md"><strong>Título</strong></a></span><span class="sxs-lookup"><span data-stu-id="b165a-110"><a href="title-summary.md"><strong>Title</strong></a></span></span></td>
<td><span data-ttu-id="b165a-111">Uma descrição desse arquivo como um pacote de instalação.</span><span class="sxs-lookup"><span data-stu-id="b165a-111">A description of this file as an installation package.</span></span> <span data-ttu-id="b165a-112">A descrição deve incluir o &quot; <a href="about-the-installer-database.md">banco de dados de instalação</a>de frase.&quot;</span><span class="sxs-lookup"><span data-stu-id="b165a-112">The description should include the phrase &quot;<a href="about-the-installer-database.md">Installation Database</a>.&quot;</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="b165a-113"><a href="subject-summary.md"><strong>Assunto</strong></a></span><span class="sxs-lookup"><span data-stu-id="b165a-113"><a href="subject-summary.md"><strong>Subject</strong></a></span></span></td>
<td><span data-ttu-id="b165a-114">O nome do produto instalado por este pacote.</span><span class="sxs-lookup"><span data-stu-id="b165a-114">The name of the product installed by this package.</span></span> <span data-ttu-id="b165a-115">Deve ser o mesmo nome que na propriedade <a href="productname.md"><strong>ProductName</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="b165a-115">This should be the same name as in the <a href="productname.md"><strong>ProductName</strong></a> property.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="b165a-116"><a href="author-summary.md"><strong>Autor</strong></a></span><span class="sxs-lookup"><span data-stu-id="b165a-116"><a href="author-summary.md"><strong>Author</strong></a></span></span></td>
<td><span data-ttu-id="b165a-117">O nome do fabricante deste produto.</span><span class="sxs-lookup"><span data-stu-id="b165a-117">The name of the manufacturer of this product.</span></span> <span data-ttu-id="b165a-118">Deve ser o mesmo nome da Propriedade do <a href="manufacturer.md"><strong>fabricante</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="b165a-118">This should be the same name as in the <a href="manufacturer.md"><strong>Manufacturer</strong></a> property.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="b165a-119"><a href="keywords-summary.md"><strong>Palavras-chave</strong></a></span><span class="sxs-lookup"><span data-stu-id="b165a-119"><a href="keywords-summary.md"><strong>Keywords</strong></a></span></span></td>
<td><span data-ttu-id="b165a-120">Uma lista de palavras-chave que podem ser usadas por navegadores de arquivos para realizar pesquisas de palavra-chaves em um arquivo.</span><span class="sxs-lookup"><span data-stu-id="b165a-120">A list of keywords that may be used by file browsers to do keyword searches for a file.</span></span> <span data-ttu-id="b165a-121">As palavras-chave devem incluir o &quot; instalador &quot; , bem como palavras-chave específicas do produto.</span><span class="sxs-lookup"><span data-stu-id="b165a-121">The keywords should include &quot;Installer&quot; as well as product-specific keywords.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="b165a-122"><a href="comments-summary.md"><strong>Comentários</strong></a></span><span class="sxs-lookup"><span data-stu-id="b165a-122"><a href="comments-summary.md"><strong>Comments</strong></a></span></span></td>
<td><span data-ttu-id="b165a-123">Contém a frase: &quot; este banco de dados do instalador contém a lógica e os requisitos necessários para instalar <<em>nome do produto</em> > .&quot;</span><span class="sxs-lookup"><span data-stu-id="b165a-123">Contains the phrase: &quot;This installer database contains the logic and data required to install <<em>product name</em>>.&quot;</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="b165a-124"><a href="template-summary.md"><strong>Modelo</strong></a> (obrigatório)</span><span class="sxs-lookup"><span data-stu-id="b165a-124"><a href="template-summary.md"><strong>Template</strong></a> (REQUIRED)</span></span></td>
<td><span data-ttu-id="b165a-125">A plataforma e as linguagens compatíveis com este pacote de instalação.</span><span class="sxs-lookup"><span data-stu-id="b165a-125">The platform and languages compatible with this installation package.</span></span> <span data-ttu-id="b165a-126">Consulte <a href="template-summary.md"><strong>modelo</strong></a> para obter a sintaxe.</span><span class="sxs-lookup"><span data-stu-id="b165a-126">See <a href="template-summary.md"><strong>Template</strong></a> for syntax.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="b165a-127"><a href="last-saved-by-summary.md"><strong>Salvo pela última vez por</strong></a></span><span class="sxs-lookup"><span data-stu-id="b165a-127"><a href="last-saved-by-summary.md"><strong>Last Saved By</strong></a></span></span></td>
<td><span data-ttu-id="b165a-128">Os desenvolvedores de ferramentas de edição de banco de dados podem usar essa propriedade durante o processo de desenvolvimento para acompanhar a última pessoa para modificar o banco de dados de instalação.</span><span class="sxs-lookup"><span data-stu-id="b165a-128">Developers of database editing tools may use this property during the development process to track the last person to modify the installation database.</span></span> <span data-ttu-id="b165a-129">Essa propriedade deve ser definida como NULL em um banco de dados de envio final.</span><span class="sxs-lookup"><span data-stu-id="b165a-129">This property should be set to Null in a final shipping database.</span></span> <span data-ttu-id="b165a-130">O instalador define essa propriedade como o valor da propriedade <a href="logonuser.md"><strong>LogonUser</strong></a> durante uma <a href="administrative-installation.md"><strong>instalação administrativa</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="b165a-130">The installer sets this property to the value of the <a href="logonuser.md"><strong>LogonUser</strong></a> property during an <a href="administrative-installation.md"><strong>administrative installation</strong></a>.</span></span> <span data-ttu-id="b165a-131">O instalador nunca usa essa propriedade e um usuário nunca precisa modificá-la.</span><span class="sxs-lookup"><span data-stu-id="b165a-131">The installer never uses this property and a user never needs to modify it.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="b165a-132"><a href="revision-number-summary.md"><strong>Número de revisão</strong></a> (obrigatório)</span><span class="sxs-lookup"><span data-stu-id="b165a-132"><a href="revision-number-summary.md"><strong>Revision Number</strong></a> (REQUIRED)</span></span></td>
<td><span data-ttu-id="b165a-133">Contém o <a href="package-codes.md">código do pacote</a> do instalador.</span><span class="sxs-lookup"><span data-stu-id="b165a-133">Contains the <a href="package-codes.md">package code</a> for the installer package.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="b165a-134"><a href="last-printed-summary.md"><strong>Última Impressão</strong></a></span><span class="sxs-lookup"><span data-stu-id="b165a-134"><a href="last-printed-summary.md"><strong>Last Printed</strong></a></span></span></td>
<td><span data-ttu-id="b165a-135">Pode ser definido como a data e a hora durante uma <a href="administrative-installation.md">instalação administrativa</a> para registro quando a imagem administrativa foi criada.</span><span class="sxs-lookup"><span data-stu-id="b165a-135">May be set to the date and time during an <a href="administrative-installation.md">administrative installation</a> to record when the administrative image was created.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="b165a-136"><a href="create-time-date-summary.md"><strong>Criar data/hora</strong></a></span><span class="sxs-lookup"><span data-stu-id="b165a-136"><a href="create-time-date-summary.md"><strong>Create Time/Date</strong></a></span></span></td>
<td><span data-ttu-id="b165a-137">A data e a hora em que este banco de dados do instalador foi criado.</span><span class="sxs-lookup"><span data-stu-id="b165a-137">The time and date when this installer database was created.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="b165a-138"><a href="last-saved-time-date-summary.md"><strong>Hora da última gravação/data</strong></a></span><span class="sxs-lookup"><span data-stu-id="b165a-138"><a href="last-saved-time-date-summary.md"><strong>Last Saved Time/Date</strong></a></span></span></td>
<td><span data-ttu-id="b165a-139">A data e a hora atuais do sistema no momento em que o banco de dados do instalador foi salvo pela última vez.</span><span class="sxs-lookup"><span data-stu-id="b165a-139">The current system time and date at the time the installer database was last saved.</span></span> <span data-ttu-id="b165a-140">Inicialmente nulo.</span><span class="sxs-lookup"><span data-stu-id="b165a-140">Initially null.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="b165a-141"><a href="page-count-summary.md"><strong>Contagem de páginas</strong></a> (obrigatória)</span><span class="sxs-lookup"><span data-stu-id="b165a-141"><a href="page-count-summary.md"><strong>Page Count</strong></a> (REQUIRED)</span></span></td>
<td><span data-ttu-id="b165a-142">Contém um valor usado para identificar a versão mínima do instalador exigida por este pacote de instalação.</span><span class="sxs-lookup"><span data-stu-id="b165a-142">Contains a value used to identify the minimum installer version required by this installation package.</span></span> <span data-ttu-id="b165a-143">Por exemplo, se o pacote exigir, no mínimo, a versão 2,0 do instalador, essa propriedade deverá ser definida como um inteiro de 200.</span><span class="sxs-lookup"><span data-stu-id="b165a-143">For example, if the package requires at minimum the 2.0 version of the installer, this property should be set to an integer of 200.</span></span>
<blockquote>
[!Note]<br />
<span data-ttu-id="b165a-144">O valor dessa propriedade deve ser 200 ou maior com <a href="64-bit-windows-installer-packages.md">pacotes de Windows Installer de 64 bits</a>.</span><span class="sxs-lookup"><span data-stu-id="b165a-144">The value of this property must be 200 or greater with <a href="64-bit-windows-installer-packages.md">64-bit Windows Installer Packages</a>.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="b165a-145"><a href="word-count-summary.md"><strong>Contagem de palavras</strong></a> (obrigatória)</span><span class="sxs-lookup"><span data-stu-id="b165a-145"><a href="word-count-summary.md"><strong>Word Count</strong></a> (REQUIRED)</span></span></td>
<td><span data-ttu-id="b165a-146">O tipo da imagem do arquivo de origem.</span><span class="sxs-lookup"><span data-stu-id="b165a-146">The type of the source file image.</span></span> <span data-ttu-id="b165a-147">Armazenado no lugar da propriedade Count padrão.</span><span class="sxs-lookup"><span data-stu-id="b165a-147">Stored in place of the standard Count property.</span></span> <span data-ttu-id="b165a-148">Essa propriedade é um campo de bits.</span><span class="sxs-lookup"><span data-stu-id="b165a-148">This property is a bit field.</span></span> <span data-ttu-id="b165a-149">Consulte o tópico <a href="word-count-summary.md"><strong>contagem de palavras</strong></a> para os valores.</span><span class="sxs-lookup"><span data-stu-id="b165a-149">See the <a href="word-count-summary.md"><strong>Word Count</strong></a> topic for the values.</span></span><br/> <span data-ttu-id="b165a-150">A partir do Windows Installer versão 4,0 no Windows Vista, essa propriedade inclui bits para especificar se são necessários privilégios elevados.</span><span class="sxs-lookup"><span data-stu-id="b165a-150">Starting with Windows Installer version 4.0 on Windows Vista, this property includes bits to specify whether elevated privileges are required.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="b165a-151"><a href="character-count-summary.md"><strong>Contagem de caracteres</strong></a></span><span class="sxs-lookup"><span data-stu-id="b165a-151"><a href="character-count-summary.md"><strong>Character Count</strong></a></span></span></td>
<td><span data-ttu-id="b165a-152">Nulo</span><span class="sxs-lookup"><span data-stu-id="b165a-152">Null</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="b165a-153"><a href="creating-application-summary.md"><strong>Criando aplicativo</strong></a></span><span class="sxs-lookup"><span data-stu-id="b165a-153"><a href="creating-application-summary.md"><strong>Creating Application</strong></a></span></span></td>
<td><span data-ttu-id="b165a-154">Contém o nome do software usado para criar este banco de dados de instalação.</span><span class="sxs-lookup"><span data-stu-id="b165a-154">Contains the name of the software used to author this installation database.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="b165a-155"><a href="security-summary.md"><strong>Segurança</strong></a></span><span class="sxs-lookup"><span data-stu-id="b165a-155"><a href="security-summary.md"><strong>Security</strong></a></span></span></td>
<td><span data-ttu-id="b165a-156">O valor dessa propriedade deve ser 2-somente leitura recomendável.</span><span class="sxs-lookup"><span data-stu-id="b165a-156">The value of this property should be 2 - Recommended read-only.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="b165a-157"><a href="codepage-summary.md"><strong>Código</strong></a></span><span class="sxs-lookup"><span data-stu-id="b165a-157"><a href="codepage-summary.md"><strong>Codepage</strong></a></span></span></td>
<td><span data-ttu-id="b165a-158">O valor numérico da página de código ANSI usada para exibir as informações de resumo.</span><span class="sxs-lookup"><span data-stu-id="b165a-158">The numeric value of the ANSI code page used to display the Summary Information.</span></span> <span data-ttu-id="b165a-159">Essa propriedade deve ser definida antes que quaisquer propriedades de cadeia de caracteres sejam definidas nas informações de resumo.</span><span class="sxs-lookup"><span data-stu-id="b165a-159">This property must be set before any string properties are set in the summary information.</span></span></td>
</tr>
</tbody>
</table>



 

## <a name="transforms"></a><span data-ttu-id="b165a-160">Transformações</span><span class="sxs-lookup"><span data-stu-id="b165a-160">Transforms</span></span>



| <span data-ttu-id="b165a-161">Propriedade Summary</span><span class="sxs-lookup"><span data-stu-id="b165a-161">Summary property</span></span>                                              | <span data-ttu-id="b165a-162">Significado dessa propriedade em uma transformação</span><span class="sxs-lookup"><span data-stu-id="b165a-162">Meaning of this property in a Transform</span></span>                                                                                                                                                                                                                                                           |
|---------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="b165a-163">**Título**</span><span class="sxs-lookup"><span data-stu-id="b165a-163">**Title**</span></span>](title-summary.md)                                | <span data-ttu-id="b165a-164">Uma descrição desse arquivo como uma transformação.</span><span class="sxs-lookup"><span data-stu-id="b165a-164">A description of this file as a transform.</span></span> <span data-ttu-id="b165a-165">A descrição deve incluir a frase: "[transformar](database-transforms.md)".</span><span class="sxs-lookup"><span data-stu-id="b165a-165">The description should include the phrase: "[Transform](database-transforms.md)."</span></span>                                                                                                                                                                     |
| [<span data-ttu-id="b165a-166">**Assunto**</span><span class="sxs-lookup"><span data-stu-id="b165a-166">**Subject**</span></span>](subject-summary.md)                            | <span data-ttu-id="b165a-167">O nome do produto instalado pelo pacote de instalação original.</span><span class="sxs-lookup"><span data-stu-id="b165a-167">The name of the product installed by the original installation package.</span></span> <span data-ttu-id="b165a-168">Deve ser o mesmo valor que a propriedade de [**Resumo do assunto**](subject-summary.md) no pacote de instalação original.</span><span class="sxs-lookup"><span data-stu-id="b165a-168">This should be the same value as the [**Subject Summary**](subject-summary.md) property in the original installation package.</span></span>                                                                                            |
| [<span data-ttu-id="b165a-169">**Autor**</span><span class="sxs-lookup"><span data-stu-id="b165a-169">**Author**</span></span>](author-summary.md)                              | <span data-ttu-id="b165a-170">O nome do fabricante desta transformação.</span><span class="sxs-lookup"><span data-stu-id="b165a-170">The name of the manufacturer of this transform.</span></span>                                                                                                                                                                                                                                                   |
| [<span data-ttu-id="b165a-171">**Palavras-chave**</span><span class="sxs-lookup"><span data-stu-id="b165a-171">**Keywords**</span></span>](keywords-summary.md)                          | <span data-ttu-id="b165a-172">Uma lista de palavras-chave que podem ser usadas por navegadores de arquivos para realizar pesquisas de palavra-chaves em um arquivo.</span><span class="sxs-lookup"><span data-stu-id="b165a-172">A list of keywords that may be used by file browsers to do keyword searches for a file.</span></span> <span data-ttu-id="b165a-173">As palavras-chave devem incluir "instalador", bem como palavras-chave específicas do produto.</span><span class="sxs-lookup"><span data-stu-id="b165a-173">The keywords should include "Installer" as well as product-specific keywords.</span></span>                                                                                                                             |
| [<span data-ttu-id="b165a-174">**Comentários**</span><span class="sxs-lookup"><span data-stu-id="b165a-174">**Comments**</span></span>](comments-summary.md)                          | <span data-ttu-id="b165a-175">Contém a frase: "esta transformação contém a lógica e os dados necessários para instalar <*nome do produto*>".</span><span class="sxs-lookup"><span data-stu-id="b165a-175">Contains the phrase: "This transform contains the logic and data required to install <*product name*>."</span></span>                                                                                                                                                                                     |
| <span data-ttu-id="b165a-176">[**Modelo**](template-summary.md) (obrigatório)</span><span class="sxs-lookup"><span data-stu-id="b165a-176">[**Template**](template-summary.md) (REQUIRED)</span></span>               | <span data-ttu-id="b165a-177">As versões de plataforma e idioma compatíveis com essa transformação.</span><span class="sxs-lookup"><span data-stu-id="b165a-177">The platform and language versions compatible with this transform.</span></span> <span data-ttu-id="b165a-178">Esse valor pode ser deixado em branco se não houver restrições.</span><span class="sxs-lookup"><span data-stu-id="b165a-178">This value may be left blank if there are no restrictions.</span></span> <span data-ttu-id="b165a-179">Apenas um idioma pode ser especificado para uma transformação.</span><span class="sxs-lookup"><span data-stu-id="b165a-179">Only one language can be specified for a transform.</span></span> <span data-ttu-id="b165a-180">Para obter mais informações sobre a sintaxe, consulte [**Template**](template-summary.md).</span><span class="sxs-lookup"><span data-stu-id="b165a-180">For more information about the syntax, see [**Template**](template-summary.md).</span></span>                                |
| [<span data-ttu-id="b165a-181">**Salvo pela última vez por**</span><span class="sxs-lookup"><span data-stu-id="b165a-181">**Last Saved By**</span></span>](last-saved-by-summary.md)                | <span data-ttu-id="b165a-182">A plataforma e as IDs de idioma que o banco de dados tem depois de ser transformado.</span><span class="sxs-lookup"><span data-stu-id="b165a-182">The platform and language ID(s) that the database has after it has been transformed.</span></span> <span data-ttu-id="b165a-183">A propriedade de [**Resumo do modelo**](template-summary.md) no novo banco de dados deve ser definida com os mesmos valores.</span><span class="sxs-lookup"><span data-stu-id="b165a-183">The [**Template Summary**](template-summary.md) property in the new database should be set to the same values.</span></span>                                                                                              |
| <span data-ttu-id="b165a-184">[**Número de revisão**](revision-number-summary.md) (obrigatório)</span><span class="sxs-lookup"><span data-stu-id="b165a-184">[**Revision Number**](revision-number-summary.md) (REQUIRED)</span></span> | <span data-ttu-id="b165a-185">Uma lista dos GUIDs de código do produto e da versão dos produtos novos e originais e o GUID do código de atualização.</span><span class="sxs-lookup"><span data-stu-id="b165a-185">A list of the product code GUIDs and version of the new and original products and the upgrade code GUID.</span></span> <span data-ttu-id="b165a-186">A lista é separada por ponto e vírgula da seguinte maneira.</span><span class="sxs-lookup"><span data-stu-id="b165a-186">The list is separated by semicolons as follows.</span></span> <span data-ttu-id="b165a-187">*Original-produto-código original-versão do produto*; Novo produto de *código novo-produto-versão*; *Atualizar código*</span><span class="sxs-lookup"><span data-stu-id="b165a-187">*Original-Product-Code Original-Product-Version*;*New-Product Code New-Product-Version*; *Upgrade-Code*</span></span><br/>                       |
| [<span data-ttu-id="b165a-188">**Última Impressão**</span><span class="sxs-lookup"><span data-stu-id="b165a-188">**Last Printed**</span></span>](last-printed-summary.md)                  | <span data-ttu-id="b165a-189">Nulo</span><span class="sxs-lookup"><span data-stu-id="b165a-189">Null</span></span>                                                                                                                                                                                                                                                                                              |
| [<span data-ttu-id="b165a-190">**Criar data/hora**</span><span class="sxs-lookup"><span data-stu-id="b165a-190">**Create Time/Date**</span></span>](create-time-date-summary.md)          | <span data-ttu-id="b165a-191">A hora e a data em que a transformação foi criada.</span><span class="sxs-lookup"><span data-stu-id="b165a-191">The time and date when the transform was created.</span></span>                                                                                                                                                                                                                                                 |
| [<span data-ttu-id="b165a-192">**Hora da última gravação/data**</span><span class="sxs-lookup"><span data-stu-id="b165a-192">**Last Saved Time/Date**</span></span>](last-saved-time-date-summary.md)  | <span data-ttu-id="b165a-193">A data e a hora atuais do sistema no momento em que a transformação foi salva.</span><span class="sxs-lookup"><span data-stu-id="b165a-193">The current system time and date at the time the transform was saved.</span></span> <span data-ttu-id="b165a-194">Inicialmente nulo.</span><span class="sxs-lookup"><span data-stu-id="b165a-194">Initially null.</span></span>                                                                                                                                                                                                             |
| <span data-ttu-id="b165a-195">[**Contagem de páginas**](page-count-summary.md) (obrigatória)</span><span class="sxs-lookup"><span data-stu-id="b165a-195">[**Page Count**](page-count-summary.md) (REQUIRED)</span></span>           | <span data-ttu-id="b165a-196">Um valor usado para indicar a versão mínima do instalador necessária para processar a transformação.</span><span class="sxs-lookup"><span data-stu-id="b165a-196">A value used to indicate the minimum installer version required to process the transform.</span></span> <span data-ttu-id="b165a-197">O valor deve ser definido como o maior dos valores de propriedade de contagem de duas [**páginas**](page-count-summary.md) que pertencem aos bancos de dados usados para gerar a transformação.</span><span class="sxs-lookup"><span data-stu-id="b165a-197">The value should be set to the greater of the two [**Page Count**](page-count-summary.md) property values that belong to the databases used to generate the transform.</span></span>                                 |
| <span data-ttu-id="b165a-198">[**Contagem de palavras**](word-count-summary.md) (obrigatória)</span><span class="sxs-lookup"><span data-stu-id="b165a-198">[**Word Count**](word-count-summary.md) (REQUIRED)</span></span>           | <span data-ttu-id="b165a-199">Nulo</span><span class="sxs-lookup"><span data-stu-id="b165a-199">Null</span></span>                                                                                                                                                                                                                                                                                              |
| [<span data-ttu-id="b165a-200">**Contagem de caracteres**</span><span class="sxs-lookup"><span data-stu-id="b165a-200">**Character Count**</span></span>](character-count-summary.md)            | <span data-ttu-id="b165a-201">Essa parte do fluxo de informações de resumo é dividida em palavras de 2 16 bits.</span><span class="sxs-lookup"><span data-stu-id="b165a-201">This part of the summary information stream is divided into two 16-bit words.</span></span> <span data-ttu-id="b165a-202">A palavra superior contém [*sinalizadores de validação de transformação*](t-gly.md).</span><span class="sxs-lookup"><span data-stu-id="b165a-202">The upper word contains [*transform validation flags*](t-gly.md).</span></span> <span data-ttu-id="b165a-203">A palavra inferior contém [*sinalizadores de condição de erro de transformação*](t-gly.md).</span><span class="sxs-lookup"><span data-stu-id="b165a-203">Lower word contains [*transform error condition flags*](t-gly.md).</span></span> |
| [<span data-ttu-id="b165a-204">**Criando aplicativo**</span><span class="sxs-lookup"><span data-stu-id="b165a-204">**Creating Application**</span></span>](creating-application-summary.md)  | <span data-ttu-id="b165a-205">Contém o nome do software usado para criar essa transformação.</span><span class="sxs-lookup"><span data-stu-id="b165a-205">Contains the name of the software used to create this transform.</span></span>                                                                                                                                                                                                                                  |
| [<span data-ttu-id="b165a-206">**Segurança**</span><span class="sxs-lookup"><span data-stu-id="b165a-206">**Security**</span></span>](security-summary.md)                          | <span data-ttu-id="b165a-207">O valor dessa propriedade deve ser de 4 impostos como somente leitura.</span><span class="sxs-lookup"><span data-stu-id="b165a-207">The value of this property should be 4 - Enforced read-only.</span></span>                                                                                                                                                                                                                                      |
| [<span data-ttu-id="b165a-208">**Código**</span><span class="sxs-lookup"><span data-stu-id="b165a-208">**Codepage**</span></span>](codepage-summary.md)                          | <span data-ttu-id="b165a-209">O valor numérico da página de código ANSI usada para exibir as informações de resumo.</span><span class="sxs-lookup"><span data-stu-id="b165a-209">The numeric value of the ANSI code page used to display the Summary Information.</span></span> <span data-ttu-id="b165a-210">Essa propriedade deve ser definida antes que as propriedades de cadeia de caracteres possam ser definidas nas informações de resumo.</span><span class="sxs-lookup"><span data-stu-id="b165a-210">This property must be set before any string properties can be set in the summary information.</span></span>                                                                                                                    |



 

## <a name="patch-packages"></a><span data-ttu-id="b165a-211">Pacotes de patch</span><span class="sxs-lookup"><span data-stu-id="b165a-211">Patch Packages</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="b165a-212">Propriedade Summary</span><span class="sxs-lookup"><span data-stu-id="b165a-212">Summary property</span></span></th>
<th><span data-ttu-id="b165a-213">Significado dessa propriedade em um pacote de patch</span><span class="sxs-lookup"><span data-stu-id="b165a-213">Meaning of this property in a Patch package</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="b165a-214"><a href="title-summary.md"><strong>Título</strong></a></span><span class="sxs-lookup"><span data-stu-id="b165a-214"><a href="title-summary.md"><strong>Title</strong></a></span></span></td>
<td><span data-ttu-id="b165a-215">Uma descrição desse arquivo como um pacote de patch.</span><span class="sxs-lookup"><span data-stu-id="b165a-215">A description of this file as a patch package.</span></span> <span data-ttu-id="b165a-216">A descrição deve incluir a frase: &quot; <a href="patch-packages.md">patch</a>.&quot;</span><span class="sxs-lookup"><span data-stu-id="b165a-216">The description should include the phrase: &quot;<a href="patch-packages.md">Patch</a>.&quot;</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="b165a-217"><a href="subject-summary.md"><strong>Assunto</strong></a></span><span class="sxs-lookup"><span data-stu-id="b165a-217"><a href="subject-summary.md"><strong>Subject</strong></a></span></span></td>
<td><span data-ttu-id="b165a-218">Uma descrição do patch que inclui o nome do produto.</span><span class="sxs-lookup"><span data-stu-id="b165a-218">A description of the patch that includes the name of the product.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="b165a-219"><a href="author-summary.md"><strong>Autor</strong></a></span><span class="sxs-lookup"><span data-stu-id="b165a-219"><a href="author-summary.md"><strong>Author</strong></a></span></span></td>
<td><span data-ttu-id="b165a-220">O nome do fabricante do pacote de patch.</span><span class="sxs-lookup"><span data-stu-id="b165a-220">The name of the manufacturer of the patch package.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="b165a-221"><a href="keywords-summary.md"><strong>Palavras-chave</strong></a></span><span class="sxs-lookup"><span data-stu-id="b165a-221"><a href="keywords-summary.md"><strong>Keywords</strong></a></span></span></td>
<td><span data-ttu-id="b165a-222">Uma lista delimitada por ponto e vírgula de fontes do patch.</span><span class="sxs-lookup"><span data-stu-id="b165a-222">A semicolon delimited list of sources of the patch.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="b165a-223"><a href="comments-summary.md"><strong>Comentários</strong></a></span><span class="sxs-lookup"><span data-stu-id="b165a-223"><a href="comments-summary.md"><strong>Comments</strong></a></span></span></td>
<td><span data-ttu-id="b165a-224">Contém a frase: &quot; esse patch contém a lógica e os dados necessários para instalar <<em>nome do produto</em> > .&quot;</span><span class="sxs-lookup"><span data-stu-id="b165a-224">Contains the phrase: &quot;This patch contains the logic and data required to install <<em>product name</em>>.&quot;</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="b165a-225"><a href="template-summary.md"><strong>Modelo</strong></a> (obrigatório)</span><span class="sxs-lookup"><span data-stu-id="b165a-225"><a href="template-summary.md"><strong>Template</strong></a> (REQUIRED)</span></span></td>
<td><span data-ttu-id="b165a-226">Uma lista delimitada por ponto e vírgula dos códigos de produto que podem aceitar esse patch.</span><span class="sxs-lookup"><span data-stu-id="b165a-226">A semicolon delimited list of the product codes that can accept this patch.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="b165a-227"><a href="last-saved-by-summary.md"><strong>Salvo pela última vez por</strong></a></span><span class="sxs-lookup"><span data-stu-id="b165a-227"><a href="last-saved-by-summary.md"><strong>Last Saved By</strong></a></span></span></td>
<td><span data-ttu-id="b165a-228">Uma lista delimitada por ponto e vírgula de nomes de subarmazenamento de transformação na ordem em que são aplicadas por esse patch.</span><span class="sxs-lookup"><span data-stu-id="b165a-228">A semicolon delimited list of transform substorage names in the order they are applied by this patch.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="b165a-229"><a href="revision-number-summary.md"><strong>Número de revisão</strong></a> (obrigatório)</span><span class="sxs-lookup"><span data-stu-id="b165a-229"><a href="revision-number-summary.md"><strong>Revision Number</strong></a> (REQUIRED)</span></span></td>
<td><span data-ttu-id="b165a-230">Contém o código de patch GUID para o patch.</span><span class="sxs-lookup"><span data-stu-id="b165a-230">Contains the GUID patch code for the patch.</span></span> <span data-ttu-id="b165a-231">Isso pode ser seguido por uma lista de GUIDs de código de patch para patches que são removidos quando esse patch é aplicado.</span><span class="sxs-lookup"><span data-stu-id="b165a-231">This may be followed by a list of patch code GUIDs for patches that are removed when this patch is applied.</span></span> <span data-ttu-id="b165a-232">Os códigos de patch são concatenados sem delimitadores separando GUIDs na lista.</span><span class="sxs-lookup"><span data-stu-id="b165a-232">The patch codes are concatenated with no delimiters separating GUIDs in the list.</span></span>
<blockquote>
[!Note]<br />
<span data-ttu-id="b165a-233">Se o pacote de patch contiver uma tabela <a href="msipatchsequence-table.md"><strong>MsiPatchSequence</strong></a> , o patch não removerá os patches listados após o GUID do patch atual.</span><span class="sxs-lookup"><span data-stu-id="b165a-233">If the patch package contains a <a href="msipatchsequence-table.md"><strong>MsiPatchSequence</strong></a> table, the patch does not remove patches listed after the current patch's GUID.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="b165a-234"><a href="last-printed-summary.md"><strong>Última Impressão</strong></a></span><span class="sxs-lookup"><span data-stu-id="b165a-234"><a href="last-printed-summary.md"><strong>Last Printed</strong></a></span></span></td>
<td><span data-ttu-id="b165a-235">Nulo</span><span class="sxs-lookup"><span data-stu-id="b165a-235">Null</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="b165a-236"><a href="create-time-date-summary.md"><strong>Criar data/hora</strong></a></span><span class="sxs-lookup"><span data-stu-id="b165a-236"><a href="create-time-date-summary.md"><strong>Create Time/Date</strong></a></span></span></td>
<td><span data-ttu-id="b165a-237">A data e a hora em que o arquivo de patch foi criado.</span><span class="sxs-lookup"><span data-stu-id="b165a-237">The time and date when patch file was created.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="b165a-238"><a href="last-saved-time-date-summary.md"><strong>Hora da última gravação/data</strong></a></span><span class="sxs-lookup"><span data-stu-id="b165a-238"><a href="last-saved-time-date-summary.md"><strong>Last Saved Time/Date</strong></a></span></span></td>
<td><span data-ttu-id="b165a-239">A data e a hora atuais do sistema no momento em que o pacote de patch foi salvo.</span><span class="sxs-lookup"><span data-stu-id="b165a-239">The current system time and date at the time the patch package was saved.</span></span> <span data-ttu-id="b165a-240">Esse valor é inicialmente nulo.</span><span class="sxs-lookup"><span data-stu-id="b165a-240">This value is initially null.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="b165a-241"><a href="page-count-summary.md"><strong>Contagem de páginas</strong></a> (obrigatória)</span><span class="sxs-lookup"><span data-stu-id="b165a-241"><a href="page-count-summary.md"><strong>Page Count</strong></a> (REQUIRED)</span></span></td>
<td><span data-ttu-id="b165a-242">Nulo</span><span class="sxs-lookup"><span data-stu-id="b165a-242">Null</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="b165a-243"><a href="word-count-summary.md"><strong>Contagem de palavras</strong></a> (obrigatória)</span><span class="sxs-lookup"><span data-stu-id="b165a-243"><a href="word-count-summary.md"><strong>Word Count</strong></a> (REQUIRED)</span></span></td>
<td><span data-ttu-id="b165a-244">Contém um valor que indica a versão de Windows Installer mínima necessária para instalar o patch.</span><span class="sxs-lookup"><span data-stu-id="b165a-244">Contains a value that indicates the minimum Windows Installer version that is required to install the patch.</span></span> <span data-ttu-id="b165a-245">Um patch com um valor de contagem de palavras de 4 requer Windows Installer versão 3,0 ou superior para que o patch seja aplicado.</span><span class="sxs-lookup"><span data-stu-id="b165a-245">A patch with a word count value of 4 requires Windows Installer version 3.0 or higher for the patch to be applied.</span></span> <span data-ttu-id="b165a-246">Um valor de 3 indica que Windows Installer versão 2,0 ou superior é necessária.</span><span class="sxs-lookup"><span data-stu-id="b165a-246">A value of 3 indicates that Windows Installer version 2.0 or higher is required.</span></span> <span data-ttu-id="b165a-247">Um valor de 2 indica que Windows Installer versão 1,2 ou superior é necessária.</span><span class="sxs-lookup"><span data-stu-id="b165a-247">A value of 2 indicates that Windows Installer version 1.2 or higher is required.</span></span> <span data-ttu-id="b165a-248">O valor padrão é 1.</span><span class="sxs-lookup"><span data-stu-id="b165a-248">The default value is 1.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="b165a-249"><a href="character-count-summary.md"><strong>Contagem de caracteres</strong></a></span><span class="sxs-lookup"><span data-stu-id="b165a-249"><a href="character-count-summary.md"><strong>Character Count</strong></a></span></span></td>
<td><span data-ttu-id="b165a-250">Nulo</span><span class="sxs-lookup"><span data-stu-id="b165a-250">Null</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="b165a-251"><a href="creating-application-summary.md"><strong>Criando aplicativo</strong></a></span><span class="sxs-lookup"><span data-stu-id="b165a-251"><a href="creating-application-summary.md"><strong>Creating Application</strong></a></span></span></td>
<td><span data-ttu-id="b165a-252">O nome do software usado para criar o patch.</span><span class="sxs-lookup"><span data-stu-id="b165a-252">The name of the software used to create the patch.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="b165a-253"><a href="security-summary.md"><strong>Segurança</strong></a></span><span class="sxs-lookup"><span data-stu-id="b165a-253"><a href="security-summary.md"><strong>Security</strong></a></span></span></td>
<td><span data-ttu-id="b165a-254">O valor dessa propriedade deve ser de 4 impostos como somente leitura.</span><span class="sxs-lookup"><span data-stu-id="b165a-254">The value of this property should be 4 - Enforced read-only.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="b165a-255"><a href="codepage-summary.md"><strong>Código</strong></a></span><span class="sxs-lookup"><span data-stu-id="b165a-255"><a href="codepage-summary.md"><strong>Codepage</strong></a></span></span></td>
<td><span data-ttu-id="b165a-256">O valor numérico da página de código ANSI usada para exibir as informações de resumo.</span><span class="sxs-lookup"><span data-stu-id="b165a-256">The numeric value of the ANSI code page used to display the Summary Information.</span></span> <span data-ttu-id="b165a-257">Essa propriedade deve ser definida antes que quaisquer propriedades de cadeia de caracteres sejam definidas nas informações de resumo.</span><span class="sxs-lookup"><span data-stu-id="b165a-257">This property must be set before any string properties are set in the summary information.</span></span></td>
</tr>
</tbody>
</table>



 

 

 




