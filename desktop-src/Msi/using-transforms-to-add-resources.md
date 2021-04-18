---
description: Os recursos necessários para a personalização de um aplicativo, como modelos corporativos, podem ser implantados com o aplicativo, incluindo uma transformação com o pacote de instalação do aplicativo.
ms.assetid: 3d9328d0-4d95-449c-bf2b-5487f7ba5971
title: Usando transformações para adicionar recursos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7c11fac7ad65601286fb550abd950bf5ac49af1f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105810311"
---
# <a name="using-transforms-to-add-resources"></a><span data-ttu-id="c76ac-103">Usando transformações para adicionar recursos</span><span class="sxs-lookup"><span data-stu-id="c76ac-103">Using Transforms to Add Resources</span></span>

<span data-ttu-id="c76ac-104">Os recursos necessários para a personalização de um aplicativo, como modelos corporativos, podem ser implantados com o aplicativo, incluindo uma transformação com o pacote de instalação do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="c76ac-104">Resources that are needed for the customization of an application, such as corporate templates, can be deployed with the application by including a transform with the application's installation package.</span></span> <span data-ttu-id="c76ac-105">As regras a seguir devem ser seguidas durante a implantação de recursos, como arquivos, chaves do registro ou atalhos, usando uma transformação.</span><span class="sxs-lookup"><span data-stu-id="c76ac-105">The following rules should be followed when deploying resources, such as files, registry keys, or shortcuts, using a transform.</span></span>

-   <span data-ttu-id="c76ac-106">A transformação deve adicionar um ou mais novos componentes ao banco de dados de instalação para conter os recursos adicionais.</span><span class="sxs-lookup"><span data-stu-id="c76ac-106">The transform should add one or more new components to the installation database to contain the additional resources.</span></span> <span data-ttu-id="c76ac-107">A transformação não deve adicionar recursos a um componente que já existe na instalação.</span><span class="sxs-lookup"><span data-stu-id="c76ac-107">The transform should not add resources to a component that already exists in the installation.</span></span>
-   <span data-ttu-id="c76ac-108">A transformação deve adicionar um ou mais novos recursos ao banco de dados de instalação para conter esses novos componentes.</span><span class="sxs-lookup"><span data-stu-id="c76ac-108">The transform should add one or more new features to the installation database to contain these new components.</span></span> <span data-ttu-id="c76ac-109">Esses novos recursos não devem ser os pais de quaisquer recursos existentes, mas novos recursos pai e filho podem ser introduzidos juntos.</span><span class="sxs-lookup"><span data-stu-id="c76ac-109">These new features should not be the parents of any existing features, but new parent and child features may be introduced together.</span></span> <span data-ttu-id="c76ac-110">Novos recursos devem receber nomes que sejam exclusivos em todas as outras transformações deste produto.</span><span class="sxs-lookup"><span data-stu-id="c76ac-110">New features should be given names that are unique across all other transforms for this product.</span></span> <span data-ttu-id="c76ac-111">Duas transformações não devem adicionar um recurso a esse produto que tenha o mesmo nome listado na coluna recurso da [tabela de recursos](feature-table.md) e que contenham componentes ou recursos diferentes.</span><span class="sxs-lookup"><span data-stu-id="c76ac-111">No two transforms should ever add a feature to this product that has the same name listed in the Feature column of the [Feature table](feature-table.md) and containing different components or resources.</span></span>

 

 



