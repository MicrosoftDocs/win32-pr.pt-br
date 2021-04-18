---
title: Estrutura RESOURCEHEADER
description: Contém informações sobre o cabeçalho de recurso em si e os dados específicos para esse recurso.
ms.assetid: e0eba7b3-a275-4ffe-9347-46361213cf48
keywords:
- Menus de estrutura RESOURCEHEADER e outros recursos
topic_type:
- apiref
api_name:
- RESOURCEHEADER
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 41b436ebd6aeb5dc31f8ed773fbe7b12a1586185
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105812304"
---
# <a name="resourceheader-structure"></a><span data-ttu-id="e6741-104">Estrutura RESOURCEHEADER</span><span class="sxs-lookup"><span data-stu-id="e6741-104">RESOURCEHEADER structure</span></span>

<span data-ttu-id="e6741-105">Contém informações sobre o cabeçalho de recurso em si e os dados específicos para esse recurso.</span><span class="sxs-lookup"><span data-stu-id="e6741-105">Contains information about the resource header itself and the data specific to this resource.</span></span> <span data-ttu-id="e6741-106">Essa estrutura não é uma estrutura verdadeira de linguagem C, pois ela contém membros de comprimento variável.</span><span class="sxs-lookup"><span data-stu-id="e6741-106">This structure is not a true C-language structure, because it contains variable-length members.</span></span> <span data-ttu-id="e6741-107">A definição de estrutura fornecida aqui é apenas para fins de explicação; Ele não está presente em nenhum arquivo de cabeçalho padrão.</span><span class="sxs-lookup"><span data-stu-id="e6741-107">The structure definition provided here is for explanation only; it is not present in any standard header file.</span></span>

## <a name="syntax"></a><span data-ttu-id="e6741-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="e6741-108">Syntax</span></span>


```C++
typedef struct {
  DWORD DataSize;
  DWORD HeaderSize;
  DWORD TYPE;
  DWORD NAME;
  DWORD DataVersion;
  WORD  MemoryFlags;
  WORD  LanguageId;
  DWORD Version;
  DWORD Characteristics;
} RESOURCEHEADER;
```



## <a name="members"></a><span data-ttu-id="e6741-109">Membros</span><span class="sxs-lookup"><span data-stu-id="e6741-109">Members</span></span>

<dl> <dt>

<span data-ttu-id="e6741-110">**DataSize**</span><span class="sxs-lookup"><span data-stu-id="e6741-110">**DataSize**</span></span>
</dt> <dd>

<span data-ttu-id="e6741-111">Tipo: **DWORD**</span><span class="sxs-lookup"><span data-stu-id="e6741-111">Type: **DWORD**</span></span>

</dd> <dd>

<span data-ttu-id="e6741-112">O tamanho, em bytes, dos dados que segue o cabeçalho do recurso para esse recurso específico.</span><span class="sxs-lookup"><span data-stu-id="e6741-112">The size, in bytes, of the data that follows the resource header for this particular resource.</span></span> <span data-ttu-id="e6741-113">Ele não inclui nenhum preenchimento de arquivo entre esse recurso e qualquer recurso que o segue no arquivo de recurso.</span><span class="sxs-lookup"><span data-stu-id="e6741-113">It does not include any file padding between this resource and any resource that follows it in the resource file.</span></span>

</dd> <dt>

<span data-ttu-id="e6741-114">**Cabeçalhosize**</span><span class="sxs-lookup"><span data-stu-id="e6741-114">**HeaderSize**</span></span>
</dt> <dd>

<span data-ttu-id="e6741-115">Tipo: **DWORD**</span><span class="sxs-lookup"><span data-stu-id="e6741-115">Type: **DWORD**</span></span>

</dd> <dd>

<span data-ttu-id="e6741-116">O tamanho, em bytes, dos dados de cabeçalho do recurso a seguir.</span><span class="sxs-lookup"><span data-stu-id="e6741-116">The size, in bytes, of the resource header data that follows.</span></span>

</dd> <dt>

<span data-ttu-id="e6741-117">**TYPE**</span><span class="sxs-lookup"><span data-stu-id="e6741-117">**TYPE**</span></span>
</dt> <dd>

<span data-ttu-id="e6741-118">Tipo: **DWORD**</span><span class="sxs-lookup"><span data-stu-id="e6741-118">Type: **DWORD**</span></span>

</dd> <dd>

<span data-ttu-id="e6741-119">O tipo de recurso.</span><span class="sxs-lookup"><span data-stu-id="e6741-119">The resource type.</span></span> <span data-ttu-id="e6741-120">O membro de **tipo** pode ser um valor numérico ou uma cadeia de caracteres Unicode terminada em nulo que especifica o nome do tipo.</span><span class="sxs-lookup"><span data-stu-id="e6741-120">The **TYPE** member can either be a numeric value or a null-terminated Unicode string that specifies the name of the type.</span></span> <span data-ttu-id="e6741-121">Consulte a seção de comentários a seguir para obter uma descrição dos membros do tipo **Name** ou **ordinal** .</span><span class="sxs-lookup"><span data-stu-id="e6741-121">See the following Remarks section for a description of **Name** or **Ordinal** type members.</span></span>

<span data-ttu-id="e6741-122">Se o membro do **tipo** for um valor numérico, ele poderá especificar um tipo de recurso padrão ou definido pelo usuário.</span><span class="sxs-lookup"><span data-stu-id="e6741-122">If the **TYPE** member is a numeric value, it can specify either a standard or a user-defined resource type.</span></span> <span data-ttu-id="e6741-123">Se o membro for uma cadeia de caracteres, ele será um tipo de recurso definido pelo usuário.</span><span class="sxs-lookup"><span data-stu-id="e6741-123">If the member is a string, then it is a user-defined resource type.</span></span> <span data-ttu-id="e6741-124">Para obter uma lista dos tipos de recursos predefinidos, consulte [tipos de recursos](/windows/desktop/menurc/resource-types).</span><span class="sxs-lookup"><span data-stu-id="e6741-124">For a list of the predefined resource types, see [Resource Types](/windows/desktop/menurc/resource-types).</span></span>

<span data-ttu-id="e6741-125">Valores menores que 256 são reservados para uso do sistema.</span><span class="sxs-lookup"><span data-stu-id="e6741-125">Values less than 256 are reserved for system use.</span></span>

</dd> <dt>

<span data-ttu-id="e6741-126">**NOME**</span><span class="sxs-lookup"><span data-stu-id="e6741-126">**NAME**</span></span>
</dt> <dd>

<span data-ttu-id="e6741-127">Tipo: **DWORD**</span><span class="sxs-lookup"><span data-stu-id="e6741-127">Type: **DWORD**</span></span>

</dd> <dd>

<span data-ttu-id="e6741-128">Um nome que identifica o recurso específico.</span><span class="sxs-lookup"><span data-stu-id="e6741-128">A name that identifies the particular resource.</span></span> <span data-ttu-id="e6741-129">O membro **Name** , como o membro **Type** , pode ser um valor numérico ou uma cadeia de caracteres Unicode terminada em nulo.</span><span class="sxs-lookup"><span data-stu-id="e6741-129">The **NAME** member, like the **TYPE** member, can either be a numeric value or a null-terminated Unicode string.</span></span> <span data-ttu-id="e6741-130">Consulte a seção de comentários a seguir para obter uma descrição dos membros do tipo **Name** ou **ordinal** .</span><span class="sxs-lookup"><span data-stu-id="e6741-130">See the following Remarks section for a description of **Name** or **Ordinal** type members.</span></span>

<span data-ttu-id="e6741-131">Você não precisa adicionar o preenchimento para o alinhamento de **DWORD** entre os membros de **tipo** e **nome** porque eles contêm dados do **Word** .</span><span class="sxs-lookup"><span data-stu-id="e6741-131">You do not need to add padding for **DWORD** alignment between the **TYPE** and **NAME** members because they contain **WORD** data.</span></span> <span data-ttu-id="e6741-132">No entanto, talvez seja necessário adicionar uma **palavra** de preenchimento após o membro **nome** para alinhar o restante do cabeçalho nos limites **DWORD** .</span><span class="sxs-lookup"><span data-stu-id="e6741-132">However, you may need to add a **WORD** of padding after the **NAME** member to align the rest of the header on **DWORD** boundaries.</span></span>

</dd> <dt>

<span data-ttu-id="e6741-133">**Versão de**</span><span class="sxs-lookup"><span data-stu-id="e6741-133">**DataVersion**</span></span>
</dt> <dd>

<span data-ttu-id="e6741-134">Tipo: **DWORD**</span><span class="sxs-lookup"><span data-stu-id="e6741-134">Type: **DWORD**</span></span>

</dd> <dd>

<span data-ttu-id="e6741-135">Uma versão de dados de recurso predefinida.</span><span class="sxs-lookup"><span data-stu-id="e6741-135">A predefined resource data version.</span></span> <span data-ttu-id="e6741-136">Isso determinará qual versão dos dados de recursos o aplicativo deve usar.</span><span class="sxs-lookup"><span data-stu-id="e6741-136">This will determine which version of the resource data the application should use.</span></span>

</dd> <dt>

<span data-ttu-id="e6741-137">**MemoryFlags**</span><span class="sxs-lookup"><span data-stu-id="e6741-137">**MemoryFlags**</span></span>
</dt> <dd>

<span data-ttu-id="e6741-138">Tipo: **Word**</span><span class="sxs-lookup"><span data-stu-id="e6741-138">Type: **WORD**</span></span>

</dd> <dd>

<span data-ttu-id="e6741-139">Um conjunto de sinalizadores de atributo que pode descrever o estado do recurso.</span><span class="sxs-lookup"><span data-stu-id="e6741-139">A set of attribute flags that can describe the state of the resource.</span></span> <span data-ttu-id="e6741-140">Modificadores no. Arquivo de script RC atribua esses atributos ao recurso.</span><span class="sxs-lookup"><span data-stu-id="e6741-140">Modifiers in the .RC script file assign these attributes to the resource.</span></span> <span data-ttu-id="e6741-141">Os identificadores de script podem atribuir os seguintes valores de sinalizador.</span><span class="sxs-lookup"><span data-stu-id="e6741-141">The script identifiers can assign the following flag values.</span></span>

<span data-ttu-id="e6741-142">Os aplicativos não usam nenhum desses atributos.</span><span class="sxs-lookup"><span data-stu-id="e6741-142">Applications do not use any of these attributes.</span></span> <span data-ttu-id="e6741-143">Os atributos são permitidos no script para compatibilidade com versões anteriores com scripts existentes, mas são ignorados.</span><span class="sxs-lookup"><span data-stu-id="e6741-143">The attributes are permitted in the script for backward compatibility with existing scripts, but they are ignored.</span></span> <span data-ttu-id="e6741-144">Os recursos são carregados quando o módulo correspondente é carregado e liberados quando o módulo é descarregado.</span><span class="sxs-lookup"><span data-stu-id="e6741-144">Resources are loaded when the corresponding module is loaded, and are freed when the module is unloaded.</span></span>

<dt>

<span id="MOVEABLE"></span><span id="moveable"></span>

<span data-ttu-id="e6741-145">**Móvel** (0x0010)</span><span class="sxs-lookup"><span data-stu-id="e6741-145">**MOVEABLE** (0x0010)</span></span>


</dt> <dd></dd> <dt>

<span id="FIXED"></span><span id="fixed"></span>

<span data-ttu-id="e6741-146">**corrigido** (~ móvel)</span><span class="sxs-lookup"><span data-stu-id="e6741-146">**FIXED** (~MOVEABLE)</span></span>


</dt> <dd></dd> <dt>

<span id="PURE"></span><span id="pure"></span>

<span data-ttu-id="e6741-147">**Puro** (0x0020)</span><span class="sxs-lookup"><span data-stu-id="e6741-147">**PURE** (0x0020)</span></span>


</dt> <dd></dd> <dt>

<span id="IMPURE"></span><span id="impure"></span>

<span data-ttu-id="e6741-148">**impuro** (~ puro)</span><span class="sxs-lookup"><span data-stu-id="e6741-148">**IMPURE** (~PURE)</span></span>


</dt> <dd></dd> <dt>

<span id="PRELOAD"></span><span id="preload"></span>

<span data-ttu-id="e6741-149">**Pré-carregar** (0x0040)</span><span class="sxs-lookup"><span data-stu-id="e6741-149">**PRELOAD** (0x0040)</span></span>


</dt> <dd></dd> <dt>

<span id="LOADONCALL"></span><span id="loadoncall"></span>

<span data-ttu-id="e6741-150">**LOADONCALL** (~ pré-carregar)</span><span class="sxs-lookup"><span data-stu-id="e6741-150">**LOADONCALL** (~PRELOAD)</span></span>


</dt> <dd></dd> <dt>

<span id="DISCARDABLE"></span><span id="discardable"></span>

<span data-ttu-id="e6741-151">**Descartado** (0x1000)</span><span class="sxs-lookup"><span data-stu-id="e6741-151">**DISCARDABLE** (0x1000)</span></span>


</dt> <dd></dd> </dl> </dd> <dt>

<span data-ttu-id="e6741-152">**LanguageId**</span><span class="sxs-lookup"><span data-stu-id="e6741-152">**LanguageId**</span></span>
</dt> <dd>

<span data-ttu-id="e6741-153">Tipo: **Word**</span><span class="sxs-lookup"><span data-stu-id="e6741-153">Type: **WORD**</span></span>

</dd> <dd>

<span data-ttu-id="e6741-154">O idioma do recurso ou conjunto de recursos.</span><span class="sxs-lookup"><span data-stu-id="e6741-154">The language for the resource or set of resources.</span></span> <span data-ttu-id="e6741-155">Defina o valor para esse membro com a instrução de definição de recurso de [linguagem](./language-statement.md) opcional.</span><span class="sxs-lookup"><span data-stu-id="e6741-155">Set the value for this member with the optional [LANGUAGE](./language-statement.md) resource definition statement.</span></span> <span data-ttu-id="e6741-156">Os parâmetros são constantes do arquivo Winnt. h.</span><span class="sxs-lookup"><span data-stu-id="e6741-156">The parameters are constants from the Winnt.h file.</span></span>

<span data-ttu-id="e6741-157">Cada recurso inclui um identificador de idioma para que o sistema ou aplicativo possa selecionar um idioma apropriado para a localidade atual do sistema.</span><span class="sxs-lookup"><span data-stu-id="e6741-157">Each resource includes a language identifier so the system or application can select a language appropriate for the current locale of the system.</span></span> <span data-ttu-id="e6741-158">Se houver vários recursos do mesmo tipo e nome que diferem apenas no idioma das cadeias de caracteres dentro dos recursos, você precisará especificar um **LanguageID** para cada um.</span><span class="sxs-lookup"><span data-stu-id="e6741-158">If there are multiple resources of the same type and name that differ only in the language of the strings within the resources, you will need to specify a **LanguageId** for each one.</span></span>

</dd> <dt>

<span data-ttu-id="e6741-159">**Versão**</span><span class="sxs-lookup"><span data-stu-id="e6741-159">**Version**</span></span>
</dt> <dd>

<span data-ttu-id="e6741-160">Tipo: **DWORD**</span><span class="sxs-lookup"><span data-stu-id="e6741-160">Type: **DWORD**</span></span>

</dd> <dd>

<span data-ttu-id="e6741-161">Um número de versão definido pelo usuário para os dados de recurso que as ferramentas podem usar para ler e gravar arquivos de recursos.</span><span class="sxs-lookup"><span data-stu-id="e6741-161">A user-defined version number for the resource data that tools can use to read and write resource files.</span></span> <span data-ttu-id="e6741-162">Defina esse valor com a instrução de definição de recurso de [versão](./version-statement.md) opcional.</span><span class="sxs-lookup"><span data-stu-id="e6741-162">Set this value with the optional [VERSION](./version-statement.md) resource definition statement.</span></span>

</dd> <dt>

<span data-ttu-id="e6741-163">**Características**</span><span class="sxs-lookup"><span data-stu-id="e6741-163">**Characteristics**</span></span>
</dt> <dd>

<span data-ttu-id="e6741-164">Tipo: **DWORD**</span><span class="sxs-lookup"><span data-stu-id="e6741-164">Type: **DWORD**</span></span>

</dd> <dd>

<span data-ttu-id="e6741-165">Especifica informações definidas pelo usuário sobre o recurso que as ferramentas podem usar para ler e gravar arquivos de recursos.</span><span class="sxs-lookup"><span data-stu-id="e6741-165">Specifies user-defined information about the resource that tools can use to read and write resource files.</span></span> <span data-ttu-id="e6741-166">Defina esse valor com a instrução de definição de recurso [características](./characteristics-statement.md) opcionais.</span><span class="sxs-lookup"><span data-stu-id="e6741-166">Set this value with the optional [CHARACTERISTICS](./characteristics-statement.md) resource definition statement.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="e6741-167">Comentários</span><span class="sxs-lookup"><span data-stu-id="e6741-167">Remarks</span></span>

<span data-ttu-id="e6741-168">Um membro de tipo de variável é chamado de **nome** ou membro **ordinal** e é usado na maioria dos lugares no arquivo de recurso onde um identificador é exibido.</span><span class="sxs-lookup"><span data-stu-id="e6741-168">A variable type member is called a **Name** or **Ordinal** member, and it is used in most places in the resource file where an identifier appears.</span></span> <span data-ttu-id="e6741-169">A primeira **palavra** de um **nome** ou membro de tipo **ordinal** indica se o membro é um valor numérico ou uma cadeia de caracteres.</span><span class="sxs-lookup"><span data-stu-id="e6741-169">The first **WORD** of a **Name** or **Ordinal** type member indicates whether the member is a numeric value or a string.</span></span> <span data-ttu-id="e6741-170">Se a primeira **palavra** no membro for igual ao valor 0xFFFF, que é um caractere Unicode inválido, a **palavra** a seguir será um número de tipo.</span><span class="sxs-lookup"><span data-stu-id="e6741-170">If the first **WORD** in the member is equal to the value 0xffff, which is an invalid Unicode character, then the following **WORD** is a type number.</span></span> <span data-ttu-id="e6741-171">Caso contrário, o membro contém uma cadeia de caracteres Unicode e a primeira **palavra** no membro é o primeiro caractere na cadeia de caracteres de nome.</span><span class="sxs-lookup"><span data-stu-id="e6741-171">Otherwise, the member contains a Unicode string and the first **WORD** in the member is the first character in the name string.</span></span> <span data-ttu-id="e6741-172">Para obter informações adicionais sobre instruções de definição de recurso, consulte [instruções de definição de recurso](./resource-definition-statements.md).</span><span class="sxs-lookup"><span data-stu-id="e6741-172">For additional information about resource definition statements, see [Resource-Definition Statements](./resource-definition-statements.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="e6741-173">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e6741-173">Requirements</span></span>



| <span data-ttu-id="e6741-174">Requisito</span><span class="sxs-lookup"><span data-stu-id="e6741-174">Requirement</span></span> | <span data-ttu-id="e6741-175">Valor</span><span class="sxs-lookup"><span data-stu-id="e6741-175">Value</span></span> |
|-------------------------------------|------------------------------------------------------------|
| <span data-ttu-id="e6741-176">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="e6741-176">Minimum supported client</span></span><br/> | <span data-ttu-id="e6741-177">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="e6741-177">Windows 2000 Professional \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="e6741-178">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="e6741-178">Minimum supported server</span></span><br/> | <span data-ttu-id="e6741-179">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="e6741-179">Windows 2000 Server \[desktop apps only\]</span></span><br/>       |



## <a name="see-also"></a><span data-ttu-id="e6741-180">Confira também</span><span class="sxs-lookup"><span data-stu-id="e6741-180">See also</span></span>

<dl> <dt>

<span data-ttu-id="e6741-181">**Conceitua**</span><span class="sxs-lookup"><span data-stu-id="e6741-181">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="e6741-182">Recursos</span><span class="sxs-lookup"><span data-stu-id="e6741-182">Resources</span></span>](resources.md)
</dt> <dt>

<span data-ttu-id="e6741-183">**Outros recursos**</span><span class="sxs-lookup"><span data-stu-id="e6741-183">**Other Resources**</span></span>
</dt> <dt>

[<span data-ttu-id="e6741-184">Instrução de características</span><span class="sxs-lookup"><span data-stu-id="e6741-184">CHARACTERISTICS Statement</span></span>](./characteristics-statement.md)
</dt> <dt>

[<span data-ttu-id="e6741-185">Instrução de linguagem</span><span class="sxs-lookup"><span data-stu-id="e6741-185">LANGUAGE Statement</span></span>](./language-statement.md)
</dt> <dt>

[<span data-ttu-id="e6741-186">Instrução de versão</span><span class="sxs-lookup"><span data-stu-id="e6741-186">VERSION Statement</span></span>](./version-statement.md)
</dt> </dl>

 

