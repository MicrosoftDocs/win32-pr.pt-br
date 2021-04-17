---
description: O ICE53 verifica as entradas na tabela de registro que gravam as informações do instalador particular ou os valores de política no registro do sistema.
ms.assetid: f5afca1f-bd36-4f95-a62a-f6b2e37238a6
title: ICE53
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c323a502642e3cf5999e6cb332a434a9fc8a41db
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105747979"
---
# <a name="ice53"></a><span data-ttu-id="d0f7b-103">ICE53</span><span class="sxs-lookup"><span data-stu-id="d0f7b-103">ICE53</span></span>

<span data-ttu-id="d0f7b-104">O ICE53 verifica as entradas na tabela de registro que gravam as informações do instalador particular ou os valores de política no registro do sistema.</span><span class="sxs-lookup"><span data-stu-id="d0f7b-104">ICE53 checks for entries in the Registry table that write private installer information or policy values to the system registry.</span></span>

## <a name="result"></a><span data-ttu-id="d0f7b-105">Resultado</span><span class="sxs-lookup"><span data-stu-id="d0f7b-105">Result</span></span>

<span data-ttu-id="d0f7b-106">ICE53 posta um aviso se a tabela do Registro especifica a gravação de informações internas ou de política no registro.</span><span class="sxs-lookup"><span data-stu-id="d0f7b-106">ICE53 posts a warning if the Registry table specifies writing internal or policy information to the registry.</span></span>

## <a name="example"></a><span data-ttu-id="d0f7b-107">Exemplo</span><span class="sxs-lookup"><span data-stu-id="d0f7b-107">Example</span></span>

<span data-ttu-id="d0f7b-108">ICE53 posta o seguinte aviso para o exemplo mostrado.</span><span class="sxs-lookup"><span data-stu-id="d0f7b-108">ICE53 posts the following warning for the example shown.</span></span>

``` syntax
Registry Key 'Registry1' writes Installer internal or policy information.
```

<span data-ttu-id="d0f7b-109">[Tabela do registro](registry-table.md) (parcial)</span><span class="sxs-lookup"><span data-stu-id="d0f7b-109">[Registry Table](registry-table.md) (partial)</span></span>



| <span data-ttu-id="d0f7b-110">Registro</span><span class="sxs-lookup"><span data-stu-id="d0f7b-110">Registry</span></span>             | <span data-ttu-id="d0f7b-111">Root</span><span class="sxs-lookup"><span data-stu-id="d0f7b-111">Root</span></span>         | <span data-ttu-id="d0f7b-112">Chave</span><span class="sxs-lookup"><span data-stu-id="d0f7b-112">Key</span></span>                                                                                                   |
|----------------------|--------------|-------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d0f7b-113">Registry1</span><span class="sxs-lookup"><span data-stu-id="d0f7b-113">Registry1</span></span><br/> | <span data-ttu-id="d0f7b-114">1</span><span class="sxs-lookup"><span data-stu-id="d0f7b-114">1</span></span><br/> | <span data-ttu-id="d0f7b-115">**Software** \\ **Políticas** \\ do **Microsoft** \\ **Windows** \\ **Instalador** \\ do **DisableRollback**</span><span class="sxs-lookup"><span data-stu-id="d0f7b-115">**Software**\\**Policies**\\**Microsoft**\\**Windows**\\**Installer**\\**DisableRollback**</span></span><br/> |



 

<span data-ttu-id="d0f7b-116">A linha da tabela do registro ' Registry1 ' grava um valor de política do sistema no registro que afeta a instalação de todos os pacotes.</span><span class="sxs-lookup"><span data-stu-id="d0f7b-116">Registry table row 'Registry1' writes a system policy value in the registry that affects the installation of all packages.</span></span> <span data-ttu-id="d0f7b-117">Dependendo do pacote, talvez seja possível desabilitar a reversão para esse pacote sozinho definindo a propriedade [**DISABLEROLLBACK**](-disablerollback.md) na [tabela de propriedades](property-table.md).</span><span class="sxs-lookup"><span data-stu-id="d0f7b-117">Depending on the package, it may be possible to disable rollback for this package alone by setting the [**DISABLEROLLBACK**](-disablerollback.md) property in the [Property table](property-table.md).</span></span> <span data-ttu-id="d0f7b-118">Consulte [Rollback Installation](rollback-installation.md).</span><span class="sxs-lookup"><span data-stu-id="d0f7b-118">See [Rollback Installation](rollback-installation.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="d0f7b-119">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="d0f7b-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d0f7b-120">Referência de ICE</span><span class="sxs-lookup"><span data-stu-id="d0f7b-120">ICE Reference</span></span>](ice-reference.md)
</dt> </dl>

 

 




