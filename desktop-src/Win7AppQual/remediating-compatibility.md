---
description: Compatibilidade com DEP/NX
ms.assetid: 18F74BA7-2729-4EB3-8E6F-4E5A8C17C317
title: Compatibilidade com DEP/NX
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cb8b46c9143ee96b8599c10d4c70276d36e20a08
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108116424"
---
# <a name="depnx-compatibility"></a>Compatibilidade com DEP/NX

Por padrão, no Windows Internet Explorer 7, o DEP/NX está desabilitado por motivos de compatibilidade. Vários Complementos populares não são compatíveis com o DEP/NX e falham quando o Windows Internet Explorer os carrega com o DEP/NX habilitado.

Normalmente, esses Complementos são criados usando uma versão mais antiga do ATL Framework. O ATL 7,1 e versões anteriores não são projetados com o recurso de segurança DEP. Felizmente, as novas versões dos Service Packs do Microsoft Windows têm novas APIs DEP/NX que permitem usar o DEP/NX e manter a compatibilidade com versões mais antigas do ATL. Essas novas APIs permitem que o Internet Explorer opte pelo DEP/NX sem causar complementos que são criados usando versões mais antigas do ATL para falhar.

Quando um complemento não é compatível com o DEP/NX e não usa uma ATL desatualizada, você pode usar uma opção Política de Grupo para recusar o DEP/NX para o Internet Explorer até que uma versão atualizada do controle quebrado seja implantada. Os administradores locais podem controlar o DEP/NX executando o Internet Explorer como administrador e desmarcando a opção **habilitar proteção de memória** no painel **avançado** de **Opções da Internet**.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Corrigindo problemas de compatibilidade em aplicativos Web usando o modo de exibição de compatibilidade](remediating-web-applications-and-add-ons.md)
</dt> </dl>

 

 
