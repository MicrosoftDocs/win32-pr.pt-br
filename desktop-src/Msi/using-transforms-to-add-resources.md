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
# <a name="using-transforms-to-add-resources"></a>Usando transformações para adicionar recursos

Os recursos necessários para a personalização de um aplicativo, como modelos corporativos, podem ser implantados com o aplicativo, incluindo uma transformação com o pacote de instalação do aplicativo. As regras a seguir devem ser seguidas durante a implantação de recursos, como arquivos, chaves do registro ou atalhos, usando uma transformação.

-   A transformação deve adicionar um ou mais novos componentes ao banco de dados de instalação para conter os recursos adicionais. A transformação não deve adicionar recursos a um componente que já existe na instalação.
-   A transformação deve adicionar um ou mais novos recursos ao banco de dados de instalação para conter esses novos componentes. Esses novos recursos não devem ser os pais de quaisquer recursos existentes, mas novos recursos pai e filho podem ser introduzidos juntos. Novos recursos devem receber nomes que sejam exclusivos em todas as outras transformações deste produto. Duas transformações não devem adicionar um recurso a esse produto que tenha o mesmo nome listado na coluna recurso da [tabela de recursos](feature-table.md) e que contenham componentes ou recursos diferentes.

 

 



