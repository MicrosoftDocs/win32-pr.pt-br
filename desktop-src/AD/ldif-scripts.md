---
title: Scripts LDIF
description: O LDAP Data Interchange Format (LDIF) é um padrão IETF (Internet Engineering Task Force) que define como importar e exportar dados de diretório entre servidores de diretório que usam provedores de serviço LDAP.
ms.assetid: a87d0d34-96c0-4cef-a38e-30a7e2291a7a
ms.tgt_platform: multiple
keywords:
- Active Directory de scripts LDIF
- Scripts LDIF Active Directory, sobre
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e228e48770e1190065a16c95b4011f794127fbdd
ms.sourcegitcommit: 3e70ae762629e244028b437420ed50b5850db4e3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/20/2020
ms.locfileid: "103917015"
---
# <a name="ldif-scripts"></a><span data-ttu-id="50273-105">Scripts LDIF</span><span class="sxs-lookup"><span data-stu-id="50273-105">LDIF Scripts</span></span>

<span data-ttu-id="50273-106">O LDAP Data Interchange Format (LDIF) é um padrão IETF (Internet Engineering Task Force) que define como importar e exportar dados de diretório entre servidores de diretório que usam provedores de serviço LDAP.</span><span class="sxs-lookup"><span data-stu-id="50273-106">The LDAP Data Interchange Format (LDIF) is an Internet Engineering Task Force (IETF) standard that defines how to import and export directory data between directory servers that use LDAP service providers.</span></span> <span data-ttu-id="50273-107">O Windows 2000 e o Windows Server 2003 incluem um utilitário de linha de comando, LDIFDE, que pode ser usado para importar objetos de diretório para Active Directory Domain Services usando arquivos LDIF.</span><span class="sxs-lookup"><span data-stu-id="50273-107">Windows 2000 and Windows Server 2003 include a command-line utility, LDIFDE, which can be used to import directory objects into Active Directory Domain Services using LDIF files.</span></span> <span data-ttu-id="50273-108">O LDIFDE permite que você defina um filtro para uma cadeia de caracteres específica a fim de Pesquisar e listar objetos de diretório no Active Directory Domain Services como arquivos LDIF que podem ser lidos facilmente por administradores de esquema.</span><span class="sxs-lookup"><span data-stu-id="50273-108">LDIFDE enables you to set a filter to a specific string in order to search for and list directory objects in Active Directory Domain Services as LDIF files which can be easily read by schema administrators.</span></span>

<span data-ttu-id="50273-109">Ao importar um arquivo Unicode, o LDIFDE importa o arquivo como Unicode se ele contiver o identificador Unicode no início do arquivo.</span><span class="sxs-lookup"><span data-stu-id="50273-109">When importing a Unicode file, LDIFDE imports the file as Unicode if it contains the Unicode identifier at the beginning of the file.</span></span> <span data-ttu-id="50273-110">Se você quiser importar um arquivo como Unicode quando ele não contiver o identificador Unicode no início do arquivo, você poderá usar a opção-u para forçá-lo a ser importado como Unicode.</span><span class="sxs-lookup"><span data-stu-id="50273-110">If you wish to import a file as Unicode when it does not contain the Unicode identifier at the beginning of the file, you can use the -u switch in order to force it to be imported as Unicode.</span></span>

<span data-ttu-id="50273-111">O modo padrão para exportar arquivos é ANSI.</span><span class="sxs-lookup"><span data-stu-id="50273-111">The default mode for exporting files is ANSI.</span></span> <span data-ttu-id="50273-112">Se houver entradas Unicode, elas serão convertidas no formato base 64.</span><span class="sxs-lookup"><span data-stu-id="50273-112">If there are Unicode entries, they will be converted into base 64 format.</span></span> <span data-ttu-id="50273-113">Para exportar um arquivo para o formato Unicode, use a opção-u.</span><span class="sxs-lookup"><span data-stu-id="50273-113">To export a file into Unicode format, use the -u switch.</span></span>

<span data-ttu-id="50273-114">Um arquivo LDIF deve aplicar alterações de esquema quando há dependências entre os atributos que são adicionados.</span><span class="sxs-lookup"><span data-stu-id="50273-114">An LDIF file must apply schema changes when there are dependencies between the attributes that are added.</span></span> <span data-ttu-id="50273-115">Por exemplo, atributos de link de encaminhamento devem ser adicionados antes do atributo back link correspondente.</span><span class="sxs-lookup"><span data-stu-id="50273-115">For example, forward link attributes should be added before the corresponding back link attribute.</span></span> <span data-ttu-id="50273-116">Você também deve atualizar o cache de esquema antes de adicionar classes que dependem de atributos ou classes adicionadas anteriormente no script de LDIF.</span><span class="sxs-lookup"><span data-stu-id="50273-116">You must also update the schema cache before adding classes that depend on attributes or classes added earlier in the LDIF script.</span></span> <span data-ttu-id="50273-117">Para obter mais informações, consulte o exemplo de código a seguir.</span><span class="sxs-lookup"><span data-stu-id="50273-117">For more information, see the following code example.</span></span>

<span data-ttu-id="50273-118">Lembre-se de que, para valores binários, você deve codificar os valores como Base64.</span><span class="sxs-lookup"><span data-stu-id="50273-118">Be aware that for binary values, you must encode the values as base64.</span></span> <span data-ttu-id="50273-119">A codificação Base64 é definida em IETF RFC 2045, seção 6,8.</span><span class="sxs-lookup"><span data-stu-id="50273-119">Base64 encoding is defined in IETF RFC 2045, Section 6.8.</span></span>

<span data-ttu-id="50273-120">Para obter mais informações sobre o formato dos arquivos LDIF, consulte [a especificação técnica do formato LDIF (LDAP Data Interchange Format)](https://www.ietf.org/rfc/rfc2849.txt) (RFC 2849) no site da Internet Engineering Task Force.</span><span class="sxs-lookup"><span data-stu-id="50273-120">For more information about the format of LDIF files, see [The LDAP Data Interchange Format (LDIF) - Technical Specification](https://www.ietf.org/rfc/rfc2849.txt) (RFC 2849) on the Internet Engineering Task Force website.</span></span>

## <a name="ntds-specific-ldif-changetypes"></a><span data-ttu-id="50273-121">ChangeTypes LDIF específico de NTDS</span><span class="sxs-lookup"><span data-stu-id="50273-121">NTDS-specific LDIF changetypes</span></span>

<span data-ttu-id="50273-122">É melhor usar ntdsSchema \* ChangeTypes em vez de chamar LDIFDE-k.</span><span class="sxs-lookup"><span data-stu-id="50273-122">It is better to use ntdsSchema\* changetypes rather than calling ldifde -k.</span></span> <span data-ttu-id="50273-123">A opção-k de ldifde ignora um conjunto maior de erros LDAP.</span><span class="sxs-lookup"><span data-stu-id="50273-123">The -k option of ldifde ignores a larger set of LDAP errors.</span></span> <span data-ttu-id="50273-124">A lista completa de erros ignorados é a seguinte:</span><span class="sxs-lookup"><span data-stu-id="50273-124">The complete list of ignored errors is as follows:</span></span>

-   <span data-ttu-id="50273-125">O objeto já é um membro do grupo.</span><span class="sxs-lookup"><span data-stu-id="50273-125">The object is already a member of the group.</span></span>
-   <span data-ttu-id="50273-126">Uma violação de classe de objeto (ou seja, a classe de objeto especificada não existe), se o objeto que está sendo importado não tiver outros atributos.</span><span class="sxs-lookup"><span data-stu-id="50273-126">An object class violation (meaning the specified object class does not exist), if the object being imported has no other attributes.</span></span>
-   <span data-ttu-id="50273-127">o objeto já existe (o **LDAP \_ já \_ existe**)</span><span class="sxs-lookup"><span data-stu-id="50273-127">object already exists (**LDAP\_ALREADY\_EXISTS**)</span></span>
-   <span data-ttu-id="50273-128">violação de restrição **( \_ \_ violação de restrição de LDAP**)</span><span class="sxs-lookup"><span data-stu-id="50273-128">constraint violation (**LDAP\_CONSTRAINT\_VIOLATION**)</span></span>
-   <span data-ttu-id="50273-129">o atributo ou o valor já existe (**\_ atributo \_ ou \_ valor LDAP \_ existe**)</span><span class="sxs-lookup"><span data-stu-id="50273-129">attribute or value already exists (**LDAP\_ATTRIBUTE\_OR\_VALUE\_EXISTS**)</span></span>
-   <span data-ttu-id="50273-130">nenhum objeto desse tipo (**LDAP \_ não é \_ tal \_ objeto**)</span><span class="sxs-lookup"><span data-stu-id="50273-130">no such object (**LDAP\_NO\_SUCH\_OBJECT**)</span></span>

<span data-ttu-id="50273-131">Os ChangeTypes a seguir são projetados especificamente para operações de atualização de esquema.</span><span class="sxs-lookup"><span data-stu-id="50273-131">The following changetypes are designed specifically for schema upgrade operations.</span></span>



| <span data-ttu-id="50273-132">ChangeType</span><span class="sxs-lookup"><span data-stu-id="50273-132">Changetype</span></span>                      | <span data-ttu-id="50273-133">Descrição</span><span class="sxs-lookup"><span data-stu-id="50273-133">Description</span></span>                                                                                                                                                                                                                                                                              |
|---------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="50273-134">**ntdsSchemaAdd**</span><span class="sxs-lookup"><span data-stu-id="50273-134">**ntdsSchemaAdd**</span></span><br/>    | <span data-ttu-id="50273-135">**ntdsSchemaAdd** corresponde a **Add** em um arquivo LDIF.</span><span class="sxs-lookup"><span data-stu-id="50273-135">**ntdsSchemaAdd** corresponds to **add** in an LDIF file.</span></span> <span data-ttu-id="50273-136">A única diferença é que o **ntdsSchemaAdd** faria com que o LDIFDE ignorasse uma operação de **adição** se o objeto já existir no esquema.</span><span class="sxs-lookup"><span data-stu-id="50273-136">The only difference is that **ntdsSchemaAdd** would cause ldifde to skip an **add** operation if the object already exists in the schema.</span></span> <span data-ttu-id="50273-137">(O **LDAP \_ já \_ existe** é ignorado.)</span><span class="sxs-lookup"><span data-stu-id="50273-137">(**LDAP\_ALREADY\_EXISTS** is ignored.)</span></span><br/>                                   |
| <span data-ttu-id="50273-138">**ntdsSchemaModify**</span><span class="sxs-lookup"><span data-stu-id="50273-138">**ntdsSchemaModify**</span></span><br/> | <span data-ttu-id="50273-139">**ntdsSchemaModify** corresponde a **Modify** em um arquivo LDIF.</span><span class="sxs-lookup"><span data-stu-id="50273-139">**ntdsSchemaModify** corresponds to **modify** in an LDIF file.</span></span> <span data-ttu-id="50273-140">A única diferença é que o **ntdsSchemaModify** faria com que o LDIFDE ignorasse uma operação de **modificação** se o objeto não fosse encontrado no esquema.</span><span class="sxs-lookup"><span data-stu-id="50273-140">The only difference is that **ntdsSchemaModify** would cause ldifde to skip an **modify** operation if the object is not found in the schema.</span></span> <span data-ttu-id="50273-141">(**LDAP \_ não \_ tal \_ objeto** é ignorado.)</span><span class="sxs-lookup"><span data-stu-id="50273-141">(**LDAP\_NO\_SUCH\_OBJECT** is ignored.)</span></span><br/>                        |
| <span data-ttu-id="50273-142">**ntdsSchemaDelete**</span><span class="sxs-lookup"><span data-stu-id="50273-142">**ntdsSchemaDelete**</span></span><br/> | <span data-ttu-id="50273-143">**ntdsSchemaDelete** corresponde a **delete** em um arquivo LDIF.</span><span class="sxs-lookup"><span data-stu-id="50273-143">**ntdsSchemaDelete** corresponds to **delete** in an LDIF file.</span></span> <span data-ttu-id="50273-144">A única diferença é que o **ntdsSchemaDelete** faria com que o LDIFDE ignorasse uma operação de **exclusão** se o objeto não fosse encontrado no esquema.</span><span class="sxs-lookup"><span data-stu-id="50273-144">The only difference is that **ntdsSchemaDelete** would cause ldifde to skip an **delete** operation if the object is not found in the schema.</span></span> <span data-ttu-id="50273-145">(**LDAP \_ não \_ tal \_ objeto** é ignorado.)</span><span class="sxs-lookup"><span data-stu-id="50273-145">(**LDAP\_NO\_SUCH\_OBJECT** is ignored.)</span></span><br/>                        |
| <span data-ttu-id="50273-146">**ntdsSchemaModRdn**</span><span class="sxs-lookup"><span data-stu-id="50273-146">**ntdsSchemaModRdn**</span></span><br/> | <span data-ttu-id="50273-147">**ntdsSchemaModRdn** corresponde a **modrdn** em um arquivo LDIF.</span><span class="sxs-lookup"><span data-stu-id="50273-147">**ntdsSchemaModRdn** corresponds to **modrdn** in an LDIF file.</span></span> <span data-ttu-id="50273-148">A única diferença é que o **ntdsSchemaModRdn** faria com que o LDIFDE ignorasse uma operação de nome diferenciado de Modify-Relative se o objeto não for encontrado no esquema.</span><span class="sxs-lookup"><span data-stu-id="50273-148">The only difference is that **ntdsSchemaModRdn** would cause ldifde to skip a modify-relative-distinguished-name operation if the object is not found in the schema.</span></span> <span data-ttu-id="50273-149">(**LDAP \_ não \_ tal \_ objeto** é ignorado.)</span><span class="sxs-lookup"><span data-stu-id="50273-149">(**LDAP\_NO\_SUCH\_OBJECT** is ignored.)</span></span><br/> |



 

## <a name="example"></a><span data-ttu-id="50273-150">Exemplo</span><span class="sxs-lookup"><span data-stu-id="50273-150">Example</span></span>

<span data-ttu-id="50273-151">O exemplo de código a seguir inclui:</span><span class="sxs-lookup"><span data-stu-id="50273-151">The following code example includes:</span></span>

-   <span data-ttu-id="50273-152">Myschemaext. ldf é um script de LDIF que contém novos atributos e classes.</span><span class="sxs-lookup"><span data-stu-id="50273-152">Myschemaext.ldf is an LDIF script that contains new attributes and classes.</span></span> <span data-ttu-id="50273-153">Lembre-se de que esse arquivo é uma versão modificada do arquivo gerado a partir de Lgetattcls.vbs.</span><span class="sxs-lookup"><span data-stu-id="50273-153">Be aware that this file is a modified version of the file generated from Lgetattcls.vbs.</span></span> <span data-ttu-id="50273-154">Além disso, lembre-se de que o atributo **My-Test-Attribute-DN-FL** foi movido para frente do **meu-Test-Attribute-DN-BL** porque o link voltar (**meu-Test-Attribute-DN-BL**) depende do link de encaminhamento (**meu-Test-Attribute-DN-FL**).</span><span class="sxs-lookup"><span data-stu-id="50273-154">Also be aware that the **My-Test-Attribute-DN-FL** attribute was moved ahead of **My-Test-Attribute-DN-BL** because the back link (**My-Test-Attribute-DN-BL**) is dependent on the forward link (**My-Test-Attribute-DN-FL**).</span></span> <span data-ttu-id="50273-155">Além disso, o atributo operacional **schemaUpdateNow** é definido em dois locais para disparar atualizações do cache de esquema, de modo que os atributos e as classes dependentes estarão disponíveis para adicionar as duas classes no script.</span><span class="sxs-lookup"><span data-stu-id="50273-155">Furthermore, the **schemaUpdateNow** operational attribute is set in two places to trigger updates of the schema cache so that dependent attributes and classes will be available for adding the two classes in the script.</span></span>
    > [!Note]  
    > <span data-ttu-id="50273-156">Consulte o tópico [obtendo uma ID de link](obtaining-a-link-id.md) para obter informações sobre a origem da ID nas instruções LinkId:.</span><span class="sxs-lookup"><span data-stu-id="50273-156">See the topic [Obtaining a Link ID](obtaining-a-link-id.md) for information about the source of the ID in the linkID: statements.</span></span>

     

-   <span data-ttu-id="50273-157">Lgetattcls.vbs é um arquivo VBScript que gera o script LDIF usado como ponto de partida para Myschemaext. ldf.</span><span class="sxs-lookup"><span data-stu-id="50273-157">Lgetattcls.vbs is a VBScript file that generates the LDIF script used as the starting point for the Myschemaext.ldf.</span></span> <span data-ttu-id="50273-158">Lembre-se de que o caminho do esquema atual é substituído por CN = Schema, CN = Configuration, DC = MyOrg, DC = com.</span><span class="sxs-lookup"><span data-stu-id="50273-158">Be aware that the current schema path is replaced by CN=Schema,CN=Configuration,DC=myorg,DC=com.</span></span> <span data-ttu-id="50273-159">Você pode substituir DC = MyOrg, DC = com para refletir o DN (nome distinto) a ser publicado no script de LDIF, garantindo que LSETATTCLS.VBS reflita a alteração em seu **sFromDN** para que o DN correto seja substituído quando o script de LDIF for aplicado.</span><span class="sxs-lookup"><span data-stu-id="50273-159">You can replace DC=myorg,DC=com to reflect the distinguished name (DN) to publish in the LDIF script  ensure that LSETATTCLS.VBS reflects the change in its **sFromDN** so that the correct DN is replaced when the LDIF script is applied.</span></span> <span data-ttu-id="50273-160">Além disso, lembre-se de que o script usa um prefixo para localizar as classes e os atributos que você também deve definir e usar um prefixo para todas as classes e atributos.</span><span class="sxs-lookup"><span data-stu-id="50273-160">Also be aware that the script uses a prefix to find the classes and attributes you should also define and use a prefix for all your classes and attributes.</span></span> <span data-ttu-id="50273-161">Para obter mais informações, consulte [nomenclatura de atributos e classes](naming-attributes-and-classes.md).</span><span class="sxs-lookup"><span data-stu-id="50273-161">For more information, see [Naming Attributes and Classes](naming-attributes-and-classes.md).</span></span> <span data-ttu-id="50273-162">Além disso, o script gera apenas os atributos necessários para os objetos **attributeSchema** e **classSchema** para o arquivo LDIF.</span><span class="sxs-lookup"><span data-stu-id="50273-162">In addition, the script outputs only the necessary attributes for the **attributeSchema** and **classSchema** objects to the LDIF file.</span></span>
-   <span data-ttu-id="50273-163">Lsetattcls.vbs é um arquivo VBScript que usa o script Myschemaext. ldf para adicionar novos atributos e classes no script.</span><span class="sxs-lookup"><span data-stu-id="50273-163">Lsetattcls.vbs is a VBScript file that uses the Myschemaext.ldf script to add the new attributes and classes in the script.</span></span> <span data-ttu-id="50273-164">Verifique se o mestre de esquema pode ser gravado antes de executar o script.</span><span class="sxs-lookup"><span data-stu-id="50273-164">Ensure that the schema master is able to be written to before running the script.</span></span>

## <a name="myschemaextldf"></a><span data-ttu-id="50273-165">MYSCHEMAEXT. LDF</span><span class="sxs-lookup"><span data-stu-id="50273-165">MYSCHEMAEXT.LDF</span></span>

``` syntax
dn: CN=My-Test-Attribute-CaseExactString,CN=Schema,CN=Configuration,DC=myorg,DC=com
changetype: add
adminDisplayName: My-Test-Attribute-CaseExactString
attributeID: 1.2.840.113556.1.4.7000.159.24.10.65
attributeSyntax: 2.5.5.3
cn: My-Test-Attribute-CaseExactString
description: Test attribute of syntax CaseExactString used to show how to add a CaseExactString attribute.
isMemberOfPartialAttributeSet: FALSE
isSingleValued: TRUE
lDAPDisplayName: myTestAttributeCaseExactString
distinguishedName: CN=My-Test-Attribute-CaseExactString,CN=Schema,CN=Configuration,DC=myorg,DC=com
objectCategory: CN=Attribute-Schema,CN=Schema,CN=Configuration,DC=myorg,DC=com
objectClass: attributeSchema
oMSyntax: 27
name: My-Test-Attribute-CaseExactString
schemaIDGUID:: 6ASznA3W0hGBpwDAT7mMGg==
searchFlags: 0
 
dn: CN=My-Test-Attribute-DN-FL,CN=Schema,CN=Configuration,DC=myorg,DC=com
changetype: add
adminDisplayName: My-Test-Attribute-DN-FL
attributeID: 1.2.840.113556.1.4.7000.159.24.10.614
attributeSyntax: 2.5.5.1
cn: My-Test-Attribute-DN-FL
description: Test forward link attribute of syntax DN used to show how to add a forward link attribute. Back link is My-Test-Attribute-DN-BL.
isMemberOfPartialAttributeSet: FALSE
isSingleValued: TRUE
lDAPDisplayName: myTestAttributeDNFL
linkID: 1.2.840.113556.1.2.50
distinguishedName: CN=My-Test-Attribute-DN-FL,CN=Schema,CN=Configuration,DC=myorg,DC=com
objectCategory: CN=Attribute-Schema,CN=Schema,CN=Configuration,DC=myorg,DC=com
objectClass: attributeSchema
oMObjectClass:: KwwCh3McAIVK
oMSyntax: 127
rangeLower: 0
rangeUpper: 257
name: My-Test-Attribute-DN-FL
schemaIDGUID:: YGLudffa0hGLEwDAT7mMGg==
searchFlags: 0
 
dn: CN=My-Test-Attribute-DN-BL,CN=Schema,CN=Configuration,DC=myorg,DC=com
changetype: add
adminDisplayName: My-Test-Attribute-DN-BL
attributeID: 1.2.840.113556.1.4.7000.159.24.10.615
attributeSyntax: 2.5.5.1
cn: My-Test-Attribute-DN-BL
description: Test back link attribute of syntax DN used to show how to add a back link attribute. Forward link is My-Test-Attribute-DN-FL.
isMemberOfPartialAttributeSet: FALSE
isSingleValued: TRUE
lDAPDisplayName: myTestAttributeDNBL
linkID: 1.2.840.113556.6.1234
distinguishedName: CN=My-Test-Attribute-DN-BL,CN=Schema,CN=Configuration,DC=myorg,DC=com
objectCategory: CN=Attribute-Schema,CN=Schema,CN=Configuration,DC=myorg,DC=com
objectClass: attributeSchema
oMObjectClass:: KwwCh3McAIVK
oMSyntax: 127
rangeLower: 0
rangeUpper: 257
name: My-Test-Attribute-DN-BL
schemaIDGUID:: jFfbhffa0hGLEwDAT7mMGg==
searchFlags: 0
 
dn: CN=My-Test-Attribute-DN-Regular,CN=Schema,CN=Configuration,DC=myorg,DC=com
changetype: add
adminDisplayName: My-Test-Attribute-DN-Regular
attributeID: 1.2.840.113556.1.4.7000.159.24.10.613
attributeSyntax: 2.5.5.12
cn: My-Test-Attribute-DN-Regular
description: Test attribute of syntax DN used to show how to add a DN attribute.
isMemberOfPartialAttributeSet: FALSE
isSingleValued: TRUE
lDAPDisplayName: myTestAttributeDNRegular
distinguishedName: CN=My-Test-Attribute-DN-Regular,CN=Schema,CN=Configuration,DC=myorg,DC=com
objectCategory: CN=Attribute-Schema,CN=Schema,CN=Configuration,DC=myorg,DC=com
objectClass: attributeSchema
oMObjectClass:: KwwCh3McAIVK
oMSyntax: 64
rangeLower: 0
rangeUpper: 257
name: My-Test-Attribute-DN-Regular
schemaIDGUID:: 5QSznA3W0hGBpwDAT7mMGg==
searchFlags: 0
 
dn: CN=My-Test-Attribute-DNString,CN=Schema,CN=Configuration,DC=myorg,DC=com
changetype: add
adminDisplayName: My-Test-Attribute-DNString
attributeID: 1.2.840.113556.1.4.7000.159.24.10.611
attributeSyntax: 2.5.5.14
cn: My-Test-Attribute-DNString
description: Test attribute of syntax DNString used to show how to add a DNString attribute.
isMemberOfPartialAttributeSet: FALSE
isSingleValued: TRUE
lDAPDisplayName: myTestAttributeDNString
distinguishedName: CN=My-Test-Attribute-DNString,CN=Schema,CN=Configuration,DC=myorg,DC=com
objectCategory: CN=Attribute-Schema,CN=Schema,CN=Configuration,DC=myorg,DC=com
objectClass: attributeSchema
oMObjectClass:: KoZIhvcUAQEBDA==
oMSyntax: 127
rangeLower: 1
rangeUpper: 64
name: My-Test-Attribute-DNString
schemaIDGUID:: 5ASznA3W0hGBpwDAT7mMGg==
searchFlags: 0

DN:
changetype: modify
add: schemaUpdateNow
schemaUpdateNow: 1
-
 
dn: CN=My-Test-Auxiliary-Class1,CN=Schema,CN=Configuration,DC=Fabrikam,DC=com
changetype: add
adminDisplayName: My-Test-Auxiliary-Class1
description: Test class used to show how to add an auxiliary class.
objectCategory: CN=Class-Schema,CN=Schema,CN=Configuration,DC=Fabrikam,DC=com
objectClass: classSchema
lDAPDisplayName: myTestAuxiliaryClass1
governsID: 1.2.840.113556.1.4.7000.159.24.10.611.11
instanceType: 4
objectClassCategory: 3
schemaIDGUID:: mmsxdsXb0hGL0AAA+HW2YA==
subClassOf: Top
mayContain: my-Test-Attribute-DNString
mustContain: description
 
DN:
changetype: modify
add: schemaUpdateNow
schemaUpdateNow: 1
-
 
dn: CN=My-Test-Structural-Class1,CN=Schema,CN=Configuration,DC=Fabrikam,DC=com
changetype: add
adminDisplayName: My-Test-Structural-Class1
auxiliaryClass: myTestAuxiliaryClass1
defaultHidingValue: FALSE
defaultObjectCategory: CN=Organizational-Unit,CN=Schema,CN=Configuration,DC=Fabrikam,DC=com
defaultSecurityDescriptor: D:(A;;RPWPCRCCDCLCLOLORCWOWDSDDTDTSW;;;DA)(A;;RPWPCRCCDCLCLORCWOWDSDDTSW;;;SY)(A;;RPLCLORC;;;AU)
admindescription: Test class used to show how to add a structure class.
objectCategory: CN=Class-Schema,CN=Schema,CN=Configuration,DC=Fabrikam,DC=com
objectClass: classSchema
lDAPDisplayName: myTestStructuralClass1
governsID: 1.2.840.113556.1.4.7000.159.24.10.611.12
mayContain: myTestAttributeDNFL
mayContain: wWWHomePage
mustContain: url
instanceType: 4
objectClassCategory: 1
possSuperiors: organizationalUnit
rDNAttID: ou
schemaIDGUID:: 1HsnsL7b0hGL0AAA+HW2YA==
subClassOf: organizationalUnit
 
DN:
changetype: modify
add: schemaUpdateNow
schemaUpdateNow: 1
-
```

## <a name="lgetattclsvbs"></a><span data-ttu-id="50273-166">LGETATTCLS.VBS</span><span class="sxs-lookup"><span data-stu-id="50273-166">LGETATTCLS.VBS</span></span>


```VB
On Error Resume Next
 
'''''''''''''''''''
' Bind to the rootDSE
'''''''''''''''''''
sPrefix = "LDAP://"
Set root= GetObject(sPrefix & "rootDSE")
If (Err.Number <> 0) Then
   BailOnFailure Err.Number, "on GetObject method"
End If
 
'''''''''''''''''''
' Get the DN for the Schema
'''''''''''''''''''
sSchema = root.Get("schemaNamingContext")
If (Err.Number <> 0) Then
   BailOnFailure Err.Number, "on Get method"
End If
 
'''''''''''''''''''
' Bind to the Schema container
'''''''''''''''''''
Set Schema= GetObject(sPrefix & sSchema )
If (Err.Number <> 0) Then
   BailOnFailure Err.Number, "on GetObject method to bind to Schema"
End If
''''''''''''''''''''
' Read the fsmoRoleOwner attribute to see which server is the schema master.
''''''''''''''''''''
sMaster = Schema.Get("fsmoRoleOwner")
If (Err.Number <> 0) Then
   BailOnFailure Err.Number, "on IADs::Get method for fsmoRoleOwner"
End If
''''''''''''''''''''
' fsmoRoleOwner attribute returns the nTDSDSA object.
' The parent is the server object.
' Bind to NTDSDSA object and get parent
''''''''''''''''''''
Set NTDS = GetObject(sPrefix & sMaster)
If (Err.Number <> 0) Then
   BailOnFailure Err.Number, "on GetObject method for NTDS"
End If
sServer = NTDS.Parent
If (Err.Number <> 0) Then
   BailOnFailure Err.Number, "on IADs::get_Parent method"
End If
''''''''''''''''''''
' Bind to server object and get the
' reference to the computer object.
''''''''''''''''''''
Set Server = GetObject(sServer)
If (Err.Number <> 0) Then
   BailOnFailure Err.Number, "on GetObject method for " & sServer
End If
'''''''''''''''''''''
' Display the DN for the computer object.
'''''''''''''''''''''
sComputerDNSName = Server.Get("DNSHostName")
strText = "Schema Master has the following DNS Name: "& sComputerDNSName
WScript.echo strText
 
sFile = "myschemaext1.ldf"
sFromDN = sSchema
sToDN = "CN=Schema,CN=Configuration,DC=myorg,DC=com"
sAttrPrefix = "My-Test"
sFilter = "(&((cn=" & sAttrPrefix & "*)(|(objectCategory=classSchema)_
(objectCategory=attributeSchema))))"
sRetAttr = "dn,adminDescription,adminDisplayName,governsID,cn,mayContain,_
mustContain,systemMayContain,systemMustContain,lDAPDisplayName,_
objectClassCategory,distinguishedName,objectCategory,objectClass,_
possSuperiors,systemPossSuperiors,subClassOf,defaultObjectCategory,_
name,schemaIDGUID,auxiliaryClass,auxiliaryClass,systemAuxiliaryClass,_
description,defaultHidingValue,rDNAttId,defaultSecurityDescriptor,_
attributeID,attributeSecurityGUID,attributeSyntax,_
isMemberOfPartialAttributeSet,isSingleValued,mAPIID,oMSyntax,rangeLower,_
rangeUpper,searchFlags,oMObjectClass,linkID"
 
' Add flag rootDN.
sCommand = "ldifde -d " & sSchema 
sCommand = sCommand & " -c " & sFromDN & " " & sToDN
' Add flag schema master.
sCommand = sCommand & " -s " & sComputerDNSName
' Add flag filename.
sCommand = sCommand & " -f " & sFile
' Add flag filter to search for attributes.
sCommand = sCommand & " -r " & sFilter
' Add flag for attributes to return.
sCommand = sCommand & " -l " & sRetAttr
 
WScript.echo sCommand
Set WshShell = Wscript.CreateObject("Wscript.Shell")
WshShell.Run (sCommand)
 
 
''''''''''''''''''''
' Display subroutines
''''''''''''''''''''
 
Sub BailOnFailure(ErrNum, ErrText) strText = "Error 0x"_
 & Hex(ErrNum) & " " & ErrText
    MsgBox strText, vbInformation, "ADSI Error"
    WScript.Quit
End Sub
```



## <a name="lsetattclsvbs"></a><span data-ttu-id="50273-167">LSETATTCLS.VBS</span><span class="sxs-lookup"><span data-stu-id="50273-167">LSETATTCLS.VBS</span></span>


```VB
On Error Resume Next
 
'''''''''''''''''''
' Bind to the rootDSE
'''''''''''''''''''
sPrefix = "LDAP://"
Set root= GetObject(sPrefix & "rootDSE")
If (Err.Number <> 0) Then
   BailOnFailure Err.Number, "on GetObject method"
End If
 
'''''''''''''''''''
' Get the DN for the Schema
'''''''''''''''''''
sSchema = root.Get("schemaNamingContext")
If (Err.Number <> 0) Then
   BailOnFailure Err.Number, "on Get method"
End If
 
'''''''''''''''''''
' Bind to the Schema container
'''''''''''''''''''
Set Schema= GetObject(sPrefix & sSchema )
If (Err.Number <> 0) Then
   BailOnFailure Err.Number, "on GetObject method to bind to Schema"
End If
''''''''''''''''''''''''''''''''''''''
' Read the fsmoRoleOwner attribute to see which server is the schema master.
''''''''''''''''''''''''''''''''''''''
sMaster = Schema.Get("fsmoRoleOwner")
If (Err.Number <> 0) Then
   BailOnFailure Err.Number, "on IADs::Get method for fsmoRoleOwner"
End If
'''''''''''''''''''''''''''
' fsmoRoleOwner attribute returns the nTDSDSA object.
' The parent is the server object.
' Bind to NTDSDSA object and get parent
'''''''''''''''''''''''''''
Set NTDS = GetObject(sPrefix & sMaster)
If (Err.Number <> 0) Then
   BailOnFailure Err.Number, "on GetObject method for NTDS"
End If
sServer = NTDS.Parent
If (Err.Number <> 0) Then
   BailOnFailure Err.Number, "on IADs::get_Parent method"
End If
''''''''''''''''''''''''
' Bind to server object
' and get the reference to the computer object.
''''''''''''''''''''''''
Set Server = GetObject(sServer)
If (Err.Number <> 0) Then
   BailOnFailure Err.Number, "on GetObject method for " & sServer
End If
sComputer = Server.Get("serverReference")
'''''''''''''''''''''
' Display the DN for the computer object.
'''''''''''''''''''''
sComputerDNSName = Server.Get("DNSHostName")
' strText = "Schema Master has the following DN: "& sComputer
strText = "Schema Master has the following DNS Name: "& sComputerDNSName
WScript.echo strText
 
sFile = "myschemaext.ldf"
sFromDN = "CN=Schema,CN=Configuration,DC=myorg,DC=com"
sToDN = sSchema
' Add flag replace fromDN with ToDN.
sCommand = "ldifde -i -k -c " & sFromDN & " " & sToDN
' Add flag schema master.
sCommand = sCommand & " -s " & sComputerDNSName
'Add flag filename.
sCommand = sCommand & " -f " & sFile
' Add flag filter to search for my attributes.
 
WScript.echo sCommand
Set WshShell = Wscript.CreateObject("Wscript.Shell")
WshShell.Run (sCommand)
 
 
''''''''''''''''''''
' Display subroutines
''''''''''''''''''''
 
Sub BailOnFailure(ErrNum, ErrText)    strText = "Error 0x" & Hex(ErrNum) & " " & ErrText
    MsgBox strText, vbInformation, "ADSI Error"
    WScript.Quit
End Sub
```



 

 





