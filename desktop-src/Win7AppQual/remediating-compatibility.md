---
description: Compatibilidade de DEP/NX
ms.assetid: 18F74BA7-2729-4EB3-8E6F-4E5A8C17C317
title: Compatibilidade de DEP/NX
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 65af83e43defb5216b176755dbc8f32067f907620bc120a16aff8b6db3392c9b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118329621"
---
# <a name="depnx-compatibility"></a>Compatibilidade de DEP/NX

Por padrão, no Windows Internet Explorer 7, o DEP/NX está desabilitado por motivos de compatibilidade. Vários complementos populares não são compatíveis com o DEP/NX e falham quando Windows Internet Explorer os carrega com o DEP/NX habilitado.

Normalmente, esses complementos são construídos usando uma versão mais antiga da estrutura da ATL. A ATL 7.1 e versões anteriores não foram projetadas com o recurso de segurança de DEP. Felizmente, as novas versões dos service packs do Microsoft Windows têm novas APIs DEP/NX que permitem que você use o DEP/NX e mantenha a compatibilidade com versões mais antigas da ATL. Essas novas APIs permitem que Internet Explorer optem por DEP/NX sem fazer com que complementos que são construídos usando versões mais antigas da ATL falhem.

Quando um complemento não é compatível com DEP/NX e não usa uma ATL desatualizada, você pode usar uma opção de Política de Grupo para não usar o DEP/NX para Internet Explorer até que uma versão atualizada do controle desfeito seja implantada. Os administradores locais podem controlar o DEP/NX executando  o Internet Explorer como  administrador e limpando a opção Habilitar proteção de memória no painel Avançado de Opções **da Internet**.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Corrigindo problemas de compatibilidade em aplicativos Web usando Modo de Exibição de Compatibilidade](remediating-web-applications-and-add-ons.md)
</dt> </dl>

 

 
