---
description: Solicita que o compilador carregue o arquivo MOF no namespace especificado como NamespacePath. Se a opção de namespace do compilador MOF-n e o \# comando pragma do namespace&\# 32; NamespacePath forem usados, o comando terá prioridade sobre a opção.
ms.assetid: d280f67a-a798-47c0-b8de-071c290dd216
ms.tgt_platform: multiple
title: namespace de pragma
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- pragma
api_type:
- NA
api_location: ''
ms.openlocfilehash: b5f5e164632fef5a41e7233caf4fd154d1dafe16
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103647696"
---
# <a name="pragma-namespace"></a><span data-ttu-id="0e45b-104">namespace de pragma</span><span class="sxs-lookup"><span data-stu-id="0e45b-104">pragma namespace</span></span>

<span data-ttu-id="0e45b-105">O comando de pré-processador do **namespace pragma** solicita que o compilador carregue o arquivo MOF no namespace especificado como *NamespacePath*.</span><span class="sxs-lookup"><span data-stu-id="0e45b-105">The **pragma namespace** preprocessor command requests that the compiler load the MOF file into the namespace specified as *namespacepath*.</span></span> <span data-ttu-id="0e45b-106">Se a opção de namespace do compilador MOF **-n** e o comando *NamespacePath* do **\# namespace pragma** forem usados, o comando terá prioridade sobre a opção.</span><span class="sxs-lookup"><span data-stu-id="0e45b-106">If both the MOF compiler **-n** namespace switch and the **\#pragma namespace** *namespacepath* command are used, the command takes priority over the switch.</span></span>

<span data-ttu-id="0e45b-107">O seguinte descreve a sintaxe:</span><span class="sxs-lookup"><span data-stu-id="0e45b-107">The following describes the syntax:</span></span>


```mof
#pragma namespace ("[Namespace]")
```



<span data-ttu-id="0e45b-108">*\[ Namespace \]* é o namespace especificado.</span><span class="sxs-lookup"><span data-stu-id="0e45b-108">*\[Namespace\]* is the specified namespace.</span></span>

<span data-ttu-id="0e45b-109">Se você não especificar esse comando ou a opção de linha de comando equivalente, o compilador MOF usará o \\ namespace raiz padrão por padrão.</span><span class="sxs-lookup"><span data-stu-id="0e45b-109">If you do not specify this command or the equivalent command-line switch, the MOF compiler uses the root\\default namespace by default.</span></span>

## <a name="remarks"></a><span data-ttu-id="0e45b-110">Comentários</span><span class="sxs-lookup"><span data-stu-id="0e45b-110">Remarks</span></span>

<span data-ttu-id="0e45b-111">Você pode exigir que os scripts e aplicativos de cliente usem uma conexão criptografada para autenticação adicionando o qualificador **RequiresEncryption** ao arquivo. MOF que cria o namespace.</span><span class="sxs-lookup"><span data-stu-id="0e45b-111">You can require that client scripts and applications use an encrypted connection for authentication by adding the **RequiresEncryption** qualifier to the .mof file that creates the namespace.</span></span> <span data-ttu-id="0e45b-112">Você também pode modificar um namespace existente adicionando esse atributo e compilar o arquivo MOF novamente.</span><span class="sxs-lookup"><span data-stu-id="0e45b-112">You can also modify an existing namespace by adding this attribute and compile the MOF file again.</span></span> <span data-ttu-id="0e45b-113">Para obter mais informações sobre como usar o **RequiresEncryption**, consulte [exigindo uma conexão criptografada para um namespace](requiring-an-encrypted-connection-to-a-namespace.md).</span><span class="sxs-lookup"><span data-stu-id="0e45b-113">For more information about how to use **RequiresEncryption**, see [Requiring an Encrypted Connection to a Namespace](requiring-an-encrypted-connection-to-a-namespace.md).</span></span>

## <a name="examples"></a><span data-ttu-id="0e45b-114">Exemplos</span><span class="sxs-lookup"><span data-stu-id="0e45b-114">Examples</span></span>

<span data-ttu-id="0e45b-115">O exemplo a seguir mostra como posicionar classes ou instâncias no namespace "raiz do \\ teste".</span><span class="sxs-lookup"><span data-stu-id="0e45b-115">The following example shows how place classes or instances in the "Root\\Test" namespace.</span></span>


```mof
#pragma namespace ("\\\\.\\Root\\Test")
```



## <a name="requirements"></a><span data-ttu-id="0e45b-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0e45b-116">Requirements</span></span>



| <span data-ttu-id="0e45b-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="0e45b-117">Requirement</span></span> | <span data-ttu-id="0e45b-118">Valor</span><span class="sxs-lookup"><span data-stu-id="0e45b-118">Value</span></span> |
|-------------------------------------|--------------------------------|
| <span data-ttu-id="0e45b-119">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="0e45b-119">Minimum supported client</span></span><br/> | <span data-ttu-id="0e45b-120">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="0e45b-120">Windows Vista</span></span><br/>       |
| <span data-ttu-id="0e45b-121">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="0e45b-121">Minimum supported server</span></span><br/> | <span data-ttu-id="0e45b-122">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="0e45b-122">Windows Server 2008</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="0e45b-123">Confira também</span><span class="sxs-lookup"><span data-stu-id="0e45b-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0e45b-124">Configurando descritores de segurança namepace</span><span class="sxs-lookup"><span data-stu-id="0e45b-124">Setting Namepace Security Descriptors</span></span>](setting-namespace-security-descriptors.md)
</dt> <dt>

[<span data-ttu-id="0e45b-125">**Qualificadores WMI padrão**</span><span class="sxs-lookup"><span data-stu-id="0e45b-125">**Standard WMI Qualifiers**</span></span>](standard-wmi-qualifiers.md)
</dt> <dt>

[<span data-ttu-id="0e45b-126">Comandos de pré-processador</span><span class="sxs-lookup"><span data-stu-id="0e45b-126">Preprocessor Commands</span></span>](preprocessor-commands.md)
</dt> </dl>

 

 




