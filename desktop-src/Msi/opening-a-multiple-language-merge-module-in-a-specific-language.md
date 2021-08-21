---
description: Ao mesclar um módulo em um banco de dados de instalação, há dois idiomas importantes.
ms.assetid: e815854f-a379-497a-ae37-b13de39dd516
title: Abrindo um módulo de mesclagem Multiple-Language em um idioma específico
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cc4dd46009f0cbe4f8c0f2cfd8b4f5dcd2caf91c7987ece7b3b032f61d9161ad
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118942867"
---
# <a name="opening-a-multiple-language-merge-module-in-a-specific-language"></a>Abrindo um módulo de mesclagem Multiple-Language em um idioma específico

Ao mesclar um módulo em um banco de dados de instalação, há dois idiomas importantes. O primeiro é o idioma do pacote de instalação de destino especificado por [**ProductLanguage**](productlanguage.md) na [tabela de propriedades](property-table.md). A segunda é o idioma do módulo de mesclagem que aparece na coluna Language da [tabela ModuleSignature](modulesignature-table.md).

O idioma do pacote de instalação pode ser passado para o módulo pela ferramenta de mesclagem quando o pacote é aberto para uma mesclagem. No entanto, às vezes pode ser necessário desconsiderar o idioma do destino e solicitar que o módulo seja aberto em outro idioma, por exemplo, um pacote em inglês instalando os recursos em inglês e alemão do módulo.

Ao abrir um módulo com uma solicitação de idioma, a ferramenta de mesclagem verifica o idioma solicitado em relação aos idiomas especificados na coluna idioma da [tabela ModuleSignature](modulesignature-table.md).

O processo a seguir é usado para determinar qual idioma usar.

**Para determinar qual idioma usar**

1.  Se o idioma na [tabela ModuleSignature](modulesignature-table.md) for igual ou mais geral do que o idioma solicitado, o módulo será aberto.
2.  Se o módulo der suporte ao idioma exato solicitado, esse idioma será usado.
3.  Se o módulo der suporte ao grupo de idiomas do idioma solicitado que o grupo de idiomas é usado, por exemplo, marque 9 se 1033 foi solicitado, mas não foi encontrado na etapa 2.
4.  Verifique se há uma transformação de idioma que altere o módulo para neutro.
5.  Se nenhuma das etapas anteriores for bem-sucedida, o módulo não oferecerá suporte ao idioma solicitado e a mesclagem falhará.

 

 



