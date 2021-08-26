---
description: Para instalar um arquivo, uma fonte ou uma chave do registro para que ele não seja removido quando o produto for desinstalado, todo o componente que contém o arquivo, a fonte ou a chave do registro deverá se tornar permanente.
ms.assetid: 99db6485-2e85-47c3-a449-ef85b7efc865
title: Instalando componentes, arquivos, fontes e chaves do registro permanentes
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 87818c2b9a80d582992dd964daa632575f51e5fa24f17a97af0191277e880df6
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120105096"
---
# <a name="installing-permanent-components-files-fonts-registry-keys"></a>Instalando componentes, arquivos, fontes e chaves do registro permanentes

Para instalar um arquivo, uma fonte ou uma chave do registro para que ele não seja removido quando o produto for desinstalado, todo o componente que contém o arquivo, a fonte ou a chave do registro deverá se tornar permanente. Para tornar um componente permanente, defina **msidbComponentAttributesPermanent** na coluna atributos da tabela de [componentes](component-table.md).

Observe que o instalador remove uma chave do registro depois de remover o último valor ou subchave sob a chave. Para impedir que uma chave do registro vazia seja removida na desinstalação, grave um valor fictício sob a chave que você precisa manter e digite + na coluna nome da [tabela do registro](registry-table.md).

 

 



