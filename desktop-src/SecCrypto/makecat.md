---
description: Uma ferramenta CryptoAPI que cria um arquivo de catálogo.
ms.assetid: 233b3644-f2a5-4166-bac0-30bf2f54e957
title: MakeCat
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2e6c2c3cb1d7df5a9f717143465d48d4c066466d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103827251"
---
# <a name="makecat"></a><span data-ttu-id="5cf6a-103">MakeCat</span><span class="sxs-lookup"><span data-stu-id="5cf6a-103">MakeCat</span></span>

<span data-ttu-id="5cf6a-104">A ferramenta MakeCat é uma ferramenta CryptoAPI que cria um arquivo de catálogo.</span><span class="sxs-lookup"><span data-stu-id="5cf6a-104">The MakeCat tool is a CryptoAPI tool that creates a catalog file.</span></span> <span data-ttu-id="5cf6a-105">O MakeCat está disponível como parte do SDK (Software Development Kit) do Microsoft Windows para Windows 7 e .NET Framework 4,0 e é instalado, por padrão, na \\ pasta bin do caminho de instalação do SDK.</span><span class="sxs-lookup"><span data-stu-id="5cf6a-105">MakeCat is available as part of the Microsoft Windows Software Development Kit (SDK) for Windows 7 and .NET Framework 4.0 and is installed, by default, in the \\Bin folder of the SDK installation path.</span></span>

<span data-ttu-id="5cf6a-106">A ferramenta MakeCat usa a seguinte sintaxe de comando:</span><span class="sxs-lookup"><span data-stu-id="5cf6a-106">The MakeCat tool uses the following command syntax:</span></span>

<span data-ttu-id="5cf6a-107">**MakeCat** \[ **-n** \| **-r** \| **-v** \] *Nome do arquivo*</span><span class="sxs-lookup"><span data-stu-id="5cf6a-107">**MakeCat** \[**-n**\|**-r**\|**-v**\] *FileName*</span></span>

## <a name="parameters"></a><span data-ttu-id="5cf6a-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="5cf6a-108">Parameters</span></span>



| <span data-ttu-id="5cf6a-109">Parâmetro</span><span class="sxs-lookup"><span data-stu-id="5cf6a-109">Parameter</span></span>             | <span data-ttu-id="5cf6a-110">Descrição</span><span class="sxs-lookup"><span data-stu-id="5cf6a-110">Description</span></span>                                                                                                                                                              |
|-----------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5cf6a-111">**-n**</span><span class="sxs-lookup"><span data-stu-id="5cf6a-111">**-n**</span></span><br/>     | <span data-ttu-id="5cf6a-112">Não pare em um erro recuperável.</span><span class="sxs-lookup"><span data-stu-id="5cf6a-112">Do not stop on a recoverable error.</span></span><br/>                                                                                                                           |
| <span data-ttu-id="5cf6a-113">**-r**</span><span class="sxs-lookup"><span data-stu-id="5cf6a-113">**-r**</span></span><br/>     | <span data-ttu-id="5cf6a-114">Força MakeCat a terminar se encontrar erros recuperáveis.</span><span class="sxs-lookup"><span data-stu-id="5cf6a-114">Forces MakeCat to end if it encounters recoverable errors.</span></span> <span data-ttu-id="5cf6a-115">Especificamente, ele terminará ao processar as entradas na seção de arquivos de catálogo de um arquivo. CDF.</span><span class="sxs-lookup"><span data-stu-id="5cf6a-115">Specifically, it will end when processing the entries in the catalog files section of a .cdf file.</span></span><br/> |
| <span data-ttu-id="5cf6a-116">**-v**</span><span class="sxs-lookup"><span data-stu-id="5cf6a-116">**-v**</span></span><br/>     | <span data-ttu-id="5cf6a-117">Extensa.</span><span class="sxs-lookup"><span data-stu-id="5cf6a-117">Verbose.</span></span> <span data-ttu-id="5cf6a-118">Exibe todas as mensagens de progresso e de erro.</span><span class="sxs-lookup"><span data-stu-id="5cf6a-118">Displays all progress and error messages.</span></span><br/>                                                                                                            |
| <span data-ttu-id="5cf6a-119">*FileName*</span><span class="sxs-lookup"><span data-stu-id="5cf6a-119">*FileName*</span></span><br/> | <span data-ttu-id="5cf6a-120">Nome do arquivo. CDF a ser analisado.</span><span class="sxs-lookup"><span data-stu-id="5cf6a-120">Name of the .cdf file to be parsed.</span></span> <span data-ttu-id="5cf6a-121">Para obter a estrutura e o conteúdo necessários, consulte comentários.</span><span class="sxs-lookup"><span data-stu-id="5cf6a-121">For required structure and contents, see Remarks.</span></span><br/>                                                                         |



 

## <a name="remarks"></a><span data-ttu-id="5cf6a-122">Comentários</span><span class="sxs-lookup"><span data-stu-id="5cf6a-122">Remarks</span></span>

<span data-ttu-id="5cf6a-123">O arquivo. CDF deve ser criado com as especificações a seguir.</span><span class="sxs-lookup"><span data-stu-id="5cf6a-123">The .cdf file must be built with the following specifications.</span></span>

``` syntax
[CatalogHeader]
Name=Name              
ResultDir=ResultDir   
PublicVersion=[|1]
CatalogVersion = [|1|2]
HashAlgorithms=[|SHA1|SHA256]
PageHashes=[true|false]
EncodingType=Encodingtype 
CATATTR1={type}:{oid}:{value} (optional)
CATATTR2={type}:{oid}:{value} (optional)

[CatalogFiles]
{reference tag}=file path and name
{reference tag}ALTSIPID={guid} (optional)
{reference tag}ATTR1={type}:{oid}:{value} (optional)
{reference tag}ATTR2={type}:{oid}:{value} (optional)
<HASH>kernel32.dll=kernel32.dll
<HASH>ntdll.dll=ntdll.dll
```

> [!Note]  
> <span data-ttu-id="5cf6a-124">A última entrada no arquivo. CDF sempre deve ter um caractere de nova linha explícito no final da linha.</span><span class="sxs-lookup"><span data-stu-id="5cf6a-124">The last entry in the .cdf file must always have an explicit newline character at the end of the line.</span></span>

 

<span data-ttu-id="5cf6a-125">A \[ \] seção CatalogHeader define informações sobre o arquivo de catálogo inteiro.</span><span class="sxs-lookup"><span data-stu-id="5cf6a-125">The \[CatalogHeader\] section defines information about the entire catalog file.</span></span>



| <span data-ttu-id="5cf6a-126">Opção</span><span class="sxs-lookup"><span data-stu-id="5cf6a-126">Option</span></span>                    | <span data-ttu-id="5cf6a-127">Descrição</span><span class="sxs-lookup"><span data-stu-id="5cf6a-127">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
|---------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5cf6a-128">Nome</span><span class="sxs-lookup"><span data-stu-id="5cf6a-128">Name</span></span><br/>           | <span data-ttu-id="5cf6a-129">Nome do arquivo de catálogo, incluindo sua extensão.</span><span class="sxs-lookup"><span data-stu-id="5cf6a-129">Name of the catalog file, including its extension.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
| <span data-ttu-id="5cf6a-130">ResultDir</span><span class="sxs-lookup"><span data-stu-id="5cf6a-130">ResultDir</span></span><br/>      | <span data-ttu-id="5cf6a-131">Diretório em que o arquivo. Cat criado será colocado.</span><span class="sxs-lookup"><span data-stu-id="5cf6a-131">Directory where the created .cat file will be placed.</span></span> <span data-ttu-id="5cf6a-132">Se não for indicado, o diretório atual padrão será usado.</span><span class="sxs-lookup"><span data-stu-id="5cf6a-132">If not indicated, the default current directory is used.</span></span> <span data-ttu-id="5cf6a-133">Se o diretório não existir, ele será criado.</span><span class="sxs-lookup"><span data-stu-id="5cf6a-133">If the directory does not exist, it is created.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| <span data-ttu-id="5cf6a-134">PublicVersion</span><span class="sxs-lookup"><span data-stu-id="5cf6a-134">PublicVersion</span></span><br/>  | <span data-ttu-id="5cf6a-135">Não há suporte para essa opção.</span><span class="sxs-lookup"><span data-stu-id="5cf6a-135">This option is not supported.</span></span> <br/> <span data-ttu-id="5cf6a-136">**Windows server 2008 R2, Windows 7, Windows server 2008, Windows Vista, Windows Server 2003 e Windows XP:** Versão do catálogo.</span><span class="sxs-lookup"><span data-stu-id="5cf6a-136">**Windows Server 2008 R2, Windows 7, Windows Server 2008, Windows Vista, Windows Server 2003 and Windows XP:** Catalog version.</span></span> <span data-ttu-id="5cf6a-137">Se for deixado em branco, o valor padrão, 1, será usado.</span><span class="sxs-lookup"><span data-stu-id="5cf6a-137">If left blank, the default value, 1, is used.</span></span><br/> <br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
| <span data-ttu-id="5cf6a-138">CatalogVersion</span><span class="sxs-lookup"><span data-stu-id="5cf6a-138">CatalogVersion</span></span><br/> | <span data-ttu-id="5cf6a-139">Versão do catálogo.</span><span class="sxs-lookup"><span data-stu-id="5cf6a-139">Catalog version.</span></span> <span data-ttu-id="5cf6a-140">Se a versão não estiver presente ou estiver definida como 1, "0x100" será passado para o parâmetro *dwPublicVersion* da função [**CryptCATOpen**](/windows/desktop/api/Mscat/nf-mscat-cryptcatopen) e um arquivo de catálogo da versão 1 será criado.</span><span class="sxs-lookup"><span data-stu-id="5cf6a-140">If the version is not present or is set to 1, then "0x100" is passed to the *dwPublicVersion* parameter of the [**CryptCATOpen**](/windows/desktop/api/Mscat/nf-mscat-cryptcatopen) function, and a version 1 catalog file is created.</span></span> <span data-ttu-id="5cf6a-141">A opção HashAlgorithms deve estar vazia ou conter SHA1.</span><span class="sxs-lookup"><span data-stu-id="5cf6a-141">The HashAlgorithms option must be empty or contain SHA1.</span></span><br/> <span data-ttu-id="5cf6a-142">Se a versão for definida como 2, "0x200" será passado para o parâmetro *dwPublicVersion* da função [**CryptCATOpen**](/windows/desktop/api/Mscat/nf-mscat-cryptcatopen) e um arquivo de catálogo da versão 2 será criado.</span><span class="sxs-lookup"><span data-stu-id="5cf6a-142">If the version is set to 2, then "0x200" is passed to the *dwPublicVersion* parameter of the [**CryptCATOpen**](/windows/desktop/api/Mscat/nf-mscat-cryptcatopen) function, and a version 2 catalog file is created.</span></span> <span data-ttu-id="5cf6a-143">A opção HashAlgorithms deve conter SHA256.</span><span class="sxs-lookup"><span data-stu-id="5cf6a-143">The HashAlgorithms option must contain SHA256.</span></span><br/> <span data-ttu-id="5cf6a-144">Se essa opção estiver presente, mas contiver qualquer valor diferente de 1 ou 2, a ferramenta MakeCat apresentará um erro.</span><span class="sxs-lookup"><span data-stu-id="5cf6a-144">If this option is present but contains any value other than 1 or 2, the MakeCat tool will error out.</span></span><br/> <span data-ttu-id="5cf6a-145">**Windows server 2008 R2, Windows 7, Windows server 2008, Windows Vista, Windows Server 2003 e Windows XP:** Não há suporte para essa opção.</span><span class="sxs-lookup"><span data-stu-id="5cf6a-145">**Windows Server 2008 R2, Windows 7, Windows Server 2008, Windows Vista, Windows Server 2003 and Windows XP:** This option is not supported.</span></span><br/> <br/> |
| <span data-ttu-id="5cf6a-146">HashAlgorithm</span><span class="sxs-lookup"><span data-stu-id="5cf6a-146">HashAlgorithms</span></span><br/> | <span data-ttu-id="5cf6a-147">Nome do algoritmo de hash usado.</span><span class="sxs-lookup"><span data-stu-id="5cf6a-147">Name of the hashing algorithm used.</span></span> <span data-ttu-id="5cf6a-148">Para obter mais informações, consulte a opção CatalogVersion.</span><span class="sxs-lookup"><span data-stu-id="5cf6a-148">For more information, see the CatalogVersion option.</span></span><br/> <span data-ttu-id="5cf6a-149">**Windows server 2008 R2, Windows 7, Windows server 2008, Windows Vista, Windows Server 2003 e Windows XP:** Não há suporte para essa opção.</span><span class="sxs-lookup"><span data-stu-id="5cf6a-149">**Windows Server 2008 R2, Windows 7, Windows Server 2008, Windows Vista, Windows Server 2003 and Windows XP:** This option is not supported.</span></span><br/> <br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
| <span data-ttu-id="5cf6a-150">PageHashes</span><span class="sxs-lookup"><span data-stu-id="5cf6a-150">PageHashes</span></span><br/>     | <span data-ttu-id="5cf6a-151">Especifica se os arquivos listados na opção devem ser incluídos em hash na <HASH> \[ \] seção CatalogFiles</span><span class="sxs-lookup"><span data-stu-id="5cf6a-151">Specifies whether to hash the files listed in the <HASH> option in the \[CatalogFiles\] section</span></span><br/> <span data-ttu-id="5cf6a-152">**Windows server 2008 R2, Windows 7, Windows server 2008, Windows Vista, Windows Server 2003 e Windows XP:** Não há suporte para essa opção.</span><span class="sxs-lookup"><span data-stu-id="5cf6a-152">**Windows Server 2008 R2, Windows 7, Windows Server 2008, Windows Vista, Windows Server 2003 and Windows XP:** This option is not supported.</span></span><br/> <br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| <span data-ttu-id="5cf6a-153">EncodingType</span><span class="sxs-lookup"><span data-stu-id="5cf6a-153">EncodingType</span></span><br/>   | <span data-ttu-id="5cf6a-154">Tipo de codificação de mensagem usado.</span><span class="sxs-lookup"><span data-stu-id="5cf6a-154">Type of message encoding used.</span></span> <span data-ttu-id="5cf6a-155">Se deixado em branco, o EncodingType padrão será a codificação \_ \_ ASN X509 de codificação ASN PKCS 7 \_ \| \_ \_ , 0x00010001.</span><span class="sxs-lookup"><span data-stu-id="5cf6a-155">If left blank, the default EncodingType is PKCS\_7\_ASN\_ENCODING \| X509\_ASN\_ENCODING, 0x00010001.</span></span> <br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |



 

<span data-ttu-id="5cf6a-156">A \[ \] seção CatalogFiles define cada membro do arquivo de catálogo com arquivos de vários tipos e atributos de vários tipos em grupos separados.</span><span class="sxs-lookup"><span data-stu-id="5cf6a-156">The \[CatalogFiles\] section defines each member of the catalog file with files of various types and attributes of various types in separate groups.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="5cf6a-157">Opção</span><span class="sxs-lookup"><span data-stu-id="5cf6a-157">Option</span></span></th>
<th><span data-ttu-id="5cf6a-158">Descrição</span><span class="sxs-lookup"><span data-stu-id="5cf6a-158">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="5cf6a-159">marca de referência</span><span class="sxs-lookup"><span data-stu-id="5cf6a-159">reference tag</span></span><br/></td>
<td><span data-ttu-id="5cf6a-160">Referência de texto para o arquivo.</span><span class="sxs-lookup"><span data-stu-id="5cf6a-160">Text reference to the file.</span></span> <span data-ttu-id="5cf6a-161">Isso pode incluir qualquer caractere de texto ASCII, exceto o sinal de igual (=).</span><span class="sxs-lookup"><span data-stu-id="5cf6a-161">This can include any ASCII text characters except the equal sign (=).</span></span> <span data-ttu-id="5cf6a-162">O sistema deve ser capaz de reproduzir essa marca após a instalação.</span><span class="sxs-lookup"><span data-stu-id="5cf6a-162">The system must be able to reproduce this tag after installation.</span></span> <br/> <span data-ttu-id="5cf6a-163">Use <HASH> como um prefixo do nome do arquivo.</span><span class="sxs-lookup"><span data-stu-id="5cf6a-163">Use <HASH> as a prefix of the file name.</span></span> <span data-ttu-id="5cf6a-164">Isso faz com que a marca seja o hash do arquivo no formato de cadeia de caracteres ASCII.</span><span class="sxs-lookup"><span data-stu-id="5cf6a-164">This results in the tag being the file's hash in ASCII string form.</span></span> <br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="5cf6a-165">caminho e nome do arquivo</span><span class="sxs-lookup"><span data-stu-id="5cf6a-165">file path and name</span></span><br/></td>
<td><span data-ttu-id="5cf6a-166">O nome do arquivo, incluindo a extensão a ser analisada e o caminho relativo para o arquivo.</span><span class="sxs-lookup"><span data-stu-id="5cf6a-166">The file name, including the extension to be parsed and the relative path to the file.</span></span> <span data-ttu-id="5cf6a-167">Qualquer tipo de arquivo que possa ser assinado com SignTool pode ser adicionado a um catálogo.</span><span class="sxs-lookup"><span data-stu-id="5cf6a-167">Any type of file that can be signed with SignTool can be added to a catalog.</span></span> <span data-ttu-id="5cf6a-168">Por exemplo, os nomes de arquivo com as seguintes extensões, entre outros, podem ser adicionados a um catálogo:. exe,. cab,. Cat,. ocx,. dll e. STL.</span><span class="sxs-lookup"><span data-stu-id="5cf6a-168">For example, file names with the following extensions, among others, can be added to a catalog: .exe, .cab, .cat, .ocx, .dll, and .stl.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="5cf6a-169">ALTSIPID</span><span class="sxs-lookup"><span data-stu-id="5cf6a-169">ALTSIPID</span></span><br/></td>
<td><span data-ttu-id="5cf6a-170">O GUID do SIP que deve ser usado para hash em vez do SIP padrão com base no tipo de arquivo.</span><span class="sxs-lookup"><span data-stu-id="5cf6a-170">SIP GUID that is to be used for hashing instead of the standard SIP based on file type.</span></span> <span data-ttu-id="5cf6a-171">Essa entrada é opcional.</span><span class="sxs-lookup"><span data-stu-id="5cf6a-171">This entry is optional.</span></span> <span data-ttu-id="5cf6a-172">Se essa entrada for omitida, o membro será transformado em hash usando o SIP padrão.</span><span class="sxs-lookup"><span data-stu-id="5cf6a-172">If this entry is omitted, the member will be hashed using the default SIP.</span></span> <span data-ttu-id="5cf6a-173">Se nenhum SIP instalado padrão for encontrado, o SIP simples será usado.</span><span class="sxs-lookup"><span data-stu-id="5cf6a-173">If no default installed SIP is found, the Flat SIP will be used.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="5cf6a-174">guid</span><span class="sxs-lookup"><span data-stu-id="5cf6a-174">guid</span></span><br/></td>
<td><span data-ttu-id="5cf6a-175">Representação de texto de um GUID.</span><span class="sxs-lookup"><span data-stu-id="5cf6a-175">Text representation of a GUID.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="5cf6a-176">ATTRx</span><span class="sxs-lookup"><span data-stu-id="5cf6a-176">ATTRx</span></span><br/></td>
<td><span data-ttu-id="5cf6a-177">Opcional.</span><span class="sxs-lookup"><span data-stu-id="5cf6a-177">Optional.</span></span> <span data-ttu-id="5cf6a-178">Atributo ou instrução sobre o arquivo ou conteúdo.</span><span class="sxs-lookup"><span data-stu-id="5cf6a-178">Attribute or statement about the file or content.</span></span> <span data-ttu-id="5cf6a-179">Pode haver qualquer número de atributos, incluindo nenhum.</span><span class="sxs-lookup"><span data-stu-id="5cf6a-179">There can be any number of attributes, including none.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="5cf6a-180">tipo</span><span class="sxs-lookup"><span data-stu-id="5cf6a-180">type</span></span><br/></td>
<td><span data-ttu-id="5cf6a-181">Define o tipo de atributo que está sendo adicionado no formato 0x00000000 (Text).</span><span class="sxs-lookup"><span data-stu-id="5cf6a-181">Defines what type of attribute is being added in the format 0x00000000 (text).</span></span> <span data-ttu-id="5cf6a-182">Essa opção pode ser uma combinação de bit-a-<strong>ou</strong> de zero ou mais dos seguintes valores:</span><span class="sxs-lookup"><span data-stu-id="5cf6a-182">This option can be a bitwise-<strong>OR</strong> combination of zero or more of the following values:</span></span><br/>
<ul>
<li><span data-ttu-id="5cf6a-183">0x10000000 o atributo autenticado (assinado, incluído no hash).</span><span class="sxs-lookup"><span data-stu-id="5cf6a-183">0x10000000 Authenticated attribute (signed, included in the hash).</span></span></li>
<li><span data-ttu-id="5cf6a-184">0x20000000 atributo não autenticado (não assinado, não incluído no hash, não verificável).</span><span class="sxs-lookup"><span data-stu-id="5cf6a-184">0x20000000 Unauthenticated attribute (unsigned, not included in the hash, not verifiable).</span></span></li>
<li><span data-ttu-id="5cf6a-185">o atributo 0x01000000 não será replicado para entradas SHA1 em um catálogo CatalogVersion 2.</span><span class="sxs-lookup"><span data-stu-id="5cf6a-185">0x01000000 Attribute will not be replicated to SHA1 entries in a CatalogVersion 2 catalog.</span></span></li>
<li><span data-ttu-id="5cf6a-186">o atributo 0x00010000 é representado em texto sem formatação.</span><span class="sxs-lookup"><span data-stu-id="5cf6a-186">0x00010000 Attribute is represented in plaintext.</span></span> <span data-ttu-id="5cf6a-187">Nenhuma conversão será feita.</span><span class="sxs-lookup"><span data-stu-id="5cf6a-187">No conversion will be done.</span></span></li>
<li><span data-ttu-id="5cf6a-188">o atributo 0x00020000 é representado na codificação base-64.</span><span class="sxs-lookup"><span data-stu-id="5cf6a-188">0x00020000 Attribute is represented in base-64 encoding.</span></span> <span data-ttu-id="5cf6a-189">Isso é usado para representar dados binários.</span><span class="sxs-lookup"><span data-stu-id="5cf6a-189">This is used to represent binary data.</span></span></li>
<li><span data-ttu-id="5cf6a-190">o atributo 0x00000001 é um par de nome-valor.</span><span class="sxs-lookup"><span data-stu-id="5cf6a-190">0x00000001 Attribute is a name-value pair.</span></span> <span data-ttu-id="5cf6a-191">Use a opção OID para o nome.</span><span class="sxs-lookup"><span data-stu-id="5cf6a-191">Use the oid option for the name.</span></span> <span data-ttu-id="5cf6a-192">Este atributo é lento; Portanto, use essa opção com moderação.</span><span class="sxs-lookup"><span data-stu-id="5cf6a-192">This attribute is slow; therefore, use this option sparingly.</span></span></li>
<li><span data-ttu-id="5cf6a-193">o atributo 0x00000002 é referenciado por um OID ( <a href="/windows/desktop/SecGloss/o-gly"><em>identificador de objeto</em></a> ).</span><span class="sxs-lookup"><span data-stu-id="5cf6a-193">0x00000002 Attribute is referenced by an <a href="/windows/desktop/SecGloss/o-gly"><em>object identifier</em></a> (OID).</span></span></li>
</ul>
<br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="5cf6a-194">oid</span><span class="sxs-lookup"><span data-stu-id="5cf6a-194">oid</span></span><br/></td>
<td><span data-ttu-id="5cf6a-195">A representação de texto da chave de referência do atributo.</span><span class="sxs-lookup"><span data-stu-id="5cf6a-195">The text representation of the attribute's reference key.</span></span> <span data-ttu-id="5cf6a-196">É um OID na forma de uma cadeia de caracteres de texto em notação quádrupla pontilhada (por exemplo, a. b. c. d) ou um nome de texto.</span><span class="sxs-lookup"><span data-stu-id="5cf6a-196">It is an OID in the form of a text string in dotted quad notation (for example, a.b.c.d) or a text Name.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="5cf6a-197">value</span><span class="sxs-lookup"><span data-stu-id="5cf6a-197">value</span></span><br/></td>
<td><span data-ttu-id="5cf6a-198">A representação de texto do valor do atributo.</span><span class="sxs-lookup"><span data-stu-id="5cf6a-198">The text representation of the value of the attribute.</span></span> <span data-ttu-id="5cf6a-199">O tipo de representação de texto usado depende do valor da opção Type.</span><span class="sxs-lookup"><span data-stu-id="5cf6a-199">The type of text representation used depends on the value of the type option.</span></span> <span data-ttu-id="5cf6a-200">Os caracteres de EOL determinam o comprimento.</span><span class="sxs-lookup"><span data-stu-id="5cf6a-200">The EOL characters determine the length.</span></span><br/></td>
</tr>
<tr class="odd">
<td><HASH><br/></td>
<td><span data-ttu-id="5cf6a-201">Aplica hash ao arquivo especificado.</span><span class="sxs-lookup"><span data-stu-id="5cf6a-201">Hashes the specified file.</span></span><br/></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="5cf6a-202">O arquivo de catálogo gerado não está assinado.</span><span class="sxs-lookup"><span data-stu-id="5cf6a-202">The generated catalog file is unsigned.</span></span> <span data-ttu-id="5cf6a-203">Se ele for assinado antes da transmissão, ele será assinado usando [SignTool](signtool.md).</span><span class="sxs-lookup"><span data-stu-id="5cf6a-203">If it is to be signed prior to transmittal, it is signed by using [SignTool](signtool.md).</span></span>

 

 
