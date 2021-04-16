---
description: A Propriedade SourcePath do objeto de sessão é uma propriedade somente leitura que fornece o caminho completo para a pasta designada na imagem de mídia ou do servidor de origem.
ms.assetid: ed8eea4f-e15e-4d56-ac0c-e18f9cb46d07
title: Propriedade Session. SourcePath
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Session.SourcePath
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 7a868e68e26f28d4fc2137e735ddc6d4c6ab0066
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105757785"
---
# <a name="sessionsourcepath-property"></a><span data-ttu-id="0a5a6-103">Propriedade Session. SourcePath</span><span class="sxs-lookup"><span data-stu-id="0a5a6-103">Session.SourcePath property</span></span>

<span data-ttu-id="0a5a6-104">A propriedade **SourcePath** do objeto de [**sessão**](session-object.md) é uma propriedade somente leitura que fornece o caminho completo para a pasta designada na imagem de mídia ou do servidor de origem.</span><span class="sxs-lookup"><span data-stu-id="0a5a6-104">The **SourcePath** property of the [**Session**](session-object.md) object is a read-only property that provides the full path to the designated folder on the source media or server image.</span></span>

<span data-ttu-id="0a5a6-105">Esta propriedade é somente para leitura.</span><span class="sxs-lookup"><span data-stu-id="0a5a6-105">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="0a5a6-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="0a5a6-106">Syntax</span></span>


```JScript
propVal = Session.SourcePath
```



## <a name="property-value"></a><span data-ttu-id="0a5a6-107">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="0a5a6-107">Property value</span></span>

<span data-ttu-id="0a5a6-108">Nome necessário diferenciar maiúsculas de minúsculas de uma propriedade de pasta, conforme especificado por uma chave primária da [tabela de diretórios](directory-table.md).</span><span class="sxs-lookup"><span data-stu-id="0a5a6-108">Required case-sensitive name of a folder property as specified by a primary key of the [Directory table](directory-table.md).</span></span> <span data-ttu-id="0a5a6-109">Um erro será gerado se a pasta não existir.</span><span class="sxs-lookup"><span data-stu-id="0a5a6-109">An error is generated if the folder does not exist.</span></span>

## <a name="remarks"></a><span data-ttu-id="0a5a6-110">Comentários</span><span class="sxs-lookup"><span data-stu-id="0a5a6-110">Remarks</span></span>

<span data-ttu-id="0a5a6-111">Se a propriedade falhar, você poderá obter informações de erro estendidas usando o método [**LastErrorRecord**](installer-lasterrorrecord.md) .</span><span class="sxs-lookup"><span data-stu-id="0a5a6-111">If the property fails, you can obtain extended error information by using the [**LastErrorRecord**](installer-lasterrorrecord.md) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="0a5a6-112">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0a5a6-112">Requirements</span></span>



| <span data-ttu-id="0a5a6-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="0a5a6-113">Requirement</span></span> | <span data-ttu-id="0a5a6-114">Valor</span><span class="sxs-lookup"><span data-stu-id="0a5a6-114">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0a5a6-115">Versão</span><span class="sxs-lookup"><span data-stu-id="0a5a6-115">Version</span></span><br/> | <span data-ttu-id="0a5a6-116">Windows Installer 5,0 no Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7.</span><span class="sxs-lookup"><span data-stu-id="0a5a6-116">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="0a5a6-117">Windows Installer 4,0 ou Windows Installer 4,5 no Windows Server 2008 ou no Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="0a5a6-117">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="0a5a6-118">Windows Installer no Windows Server 2003 ou no Windows XP</span><span class="sxs-lookup"><span data-stu-id="0a5a6-118">Windows Installer on Windows Server 2003 or Windows XP</span></span><br/> |
| <span data-ttu-id="0a5a6-119">DLL</span><span class="sxs-lookup"><span data-stu-id="0a5a6-119">DLL</span></span><br/>     | <dl> <span data-ttu-id="0a5a6-120"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0a5a6-120"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                      |
| <span data-ttu-id="0a5a6-121">IID</span><span class="sxs-lookup"><span data-stu-id="0a5a6-121">IID</span></span><br/>     | <span data-ttu-id="0a5a6-122">IID \_ ISession é definido como 000C109E-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="0a5a6-122">IID\_ISession is defined as 000C109E-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                             |



 

 




