---
description: ICE99 verifica se nenhum nome de propriedade inserido na tabela de diretório duplica um nome reservado para o uso público ou privado do Windows Installer.
ms.assetid: a7657c14-6542-4a7b-a8f7-727b109cfc39
title: ICE99
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f7d70aeaf6480e45db5b47f76434f93e49adf317
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103662335"
---
# <a name="ice99"></a><span data-ttu-id="60722-103">ICE99</span><span class="sxs-lookup"><span data-stu-id="60722-103">ICE99</span></span>

<span data-ttu-id="60722-104">ICE99 verifica se nenhum nome de propriedade inserido na tabela de [diretório](directory-table.md) duplica um nome reservado para o uso público ou privado do Windows Installer.</span><span class="sxs-lookup"><span data-stu-id="60722-104">ICE99 verifies that no property name entered in the [Directory](directory-table.md) table duplicates a name reserved for the public or private use of the Windows Installer.</span></span>

## <a name="result"></a><span data-ttu-id="60722-105">Resultado</span><span class="sxs-lookup"><span data-stu-id="60722-105">Result</span></span>

<span data-ttu-id="60722-106">ICE99 posta o erro a seguir.</span><span class="sxs-lookup"><span data-stu-id="60722-106">ICE99 posts the following error.</span></span>



| <span data-ttu-id="60722-107">Erro de ICE99</span><span class="sxs-lookup"><span data-stu-id="60722-107">ICE99 error</span></span>                                                                                                      | <span data-ttu-id="60722-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="60722-108">Description</span></span>                                                                                                                                   |
|------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="60722-109">O nome do diretório: \[ 1 \] é o mesmo que uma das propriedades públicas do MSI e pode causar efeitos colaterais imprevistos.</span><span class="sxs-lookup"><span data-stu-id="60722-109">The directory name: \[1\] is the same as one of the MSI Public Properties and can cause unforeseen side effects.</span></span> | <span data-ttu-id="60722-110">O valor na coluna Directory da tabela de [diretórios](directory-table.md) duplica um nome de propriedade reservado pelo Windows Installer.</span><span class="sxs-lookup"><span data-stu-id="60722-110">The value in the Directory column of the [Directory](directory-table.md) table duplicates a property name reserved by the Windows Installer.</span></span> |



 

## <a name="example"></a><span data-ttu-id="60722-111">Exemplo</span><span class="sxs-lookup"><span data-stu-id="60722-111">Example</span></span>

<span data-ttu-id="60722-112">ICE99 relata o seguinte erro para o exemplo:</span><span class="sxs-lookup"><span data-stu-id="60722-112">ICE99 reports the following error for the example:</span></span>

``` syntax
CustomActionData is the same as one of the MSI Public Properties and can cause unforeseen side effects.
```

<span data-ttu-id="60722-113">[Diretório](directory-table.md) (parcial)</span><span class="sxs-lookup"><span data-stu-id="60722-113">[Directory](directory-table.md) (partial)</span></span>



| <span data-ttu-id="60722-114">Diretório</span><span class="sxs-lookup"><span data-stu-id="60722-114">Directory</span></span>        | <span data-ttu-id="60722-115">Pai do diretório \_</span><span class="sxs-lookup"><span data-stu-id="60722-115">Directory\_Parent</span></span> | <span data-ttu-id="60722-116">DefaultDir</span><span class="sxs-lookup"><span data-stu-id="60722-116">DefaultDir</span></span> |
|------------------|-------------------|------------|
| <span data-ttu-id="60722-117">CustomActionData</span><span class="sxs-lookup"><span data-stu-id="60722-117">CustomActionData</span></span> |                   |            |



 

<span data-ttu-id="60722-118">Para corrigir esse aviso, você deve alterar o nome de CustomActionData.</span><span class="sxs-lookup"><span data-stu-id="60722-118">To correct this warning you should change the name of CustomActionData.</span></span>

## <a name="related-topics"></a><span data-ttu-id="60722-119">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="60722-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="60722-120">Referência de ICE</span><span class="sxs-lookup"><span data-stu-id="60722-120">ICE Reference</span></span>](ice-reference.md)
</dt> <dt>

[<span data-ttu-id="60722-121">Tabela de diretórios</span><span class="sxs-lookup"><span data-stu-id="60722-121">Directory Table</span></span>](directory-table.md)
</dt> <dt>

[<span data-ttu-id="60722-122">Sem suporte no Windows Installer 3,0 e versões anteriores</span><span class="sxs-lookup"><span data-stu-id="60722-122">Not Supported in Windows Installer 3.0 and earlier</span></span>](not-supported-in-windows-installer-version-3-0.md)
</dt> </dl>

 

 



