---
description: Para instalar um arquivo, uma fonte ou uma chave do registro para que ele não seja removido quando o produto for desinstalado, todo o componente que contém o arquivo, a fonte ou a chave do registro deverá se tornar permanente.
ms.assetid: 99db6485-2e85-47c3-a449-ef85b7efc865
title: Instalando componentes, arquivos, fontes e chaves do registro permanentes
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bd9a6e77f2e6bb2d8d7a6f48d80f6855906e4d93
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104011814"
---
# <a name="installing-permanent-components-files-fonts-registry-keys"></a>Instalando componentes, arquivos, fontes e chaves do registro permanentes

Para instalar um arquivo, uma fonte ou uma chave do registro para que ele não seja removido quando o produto for desinstalado, todo o componente que contém o arquivo, a fonte ou a chave do registro deverá se tornar permanente. Para tornar um componente permanente, defina **msidbComponentAttributesPermanent** na coluna atributos da tabela de [componentes](component-table.md).

Observe que o instalador remove uma chave do registro depois de remover o último valor ou subchave sob a chave. Para impedir que uma chave do registro vazia seja removida na desinstalação, grave um valor fictício sob a chave que você precisa manter e digite + na coluna nome da [tabela do registro](registry-table.md).

 

 



