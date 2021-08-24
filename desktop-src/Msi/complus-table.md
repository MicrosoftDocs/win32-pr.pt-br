---
description: A tabela Complus contém as informações necessárias para instalar aplicativos COM+.
ms.assetid: 0c9a7469-5959-45ad-b84d-6cfd3e169ff6
title: Tabela complus
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f77885688226689e5d81e074b1a9a28ef3801aaeba5febf51165377ac9ad9e65
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118144967"
---
# <a name="complus-table"></a>Tabela complus

A tabela Complus contém as informações necessárias para instalar aplicativos COM+.

A tabela Complus tem as seguintes colunas.



| Coluna      | Tipo                         | Chave | Nullable |
|-------------|------------------------------|-----|----------|
| Componente\_ | [Identificador](identifier.md) | Y   | N        |
| ExpType     | [Inteiro](integer.md)       | N   | Y        |



 

## <a name="columns"></a>Colunas

<dl> <dt>

<span id="Component_"></span><span id="component_"></span><span id="COMPONENT_"></span>Componente\_
</dt> <dd>

Uma chave externa na primeira coluna da [tabela Componente](component-table.md). Esse é o componente que contém o aplicativo COM+.

</dd> <dt>

<span id="ExpType"></span><span id="exptype"></span><span id="EXPTYPE"></span>ExpType
</dt> <dd>

Exportar sinalizadores usados durante a geração do arquivo .msi dados. Para obter mais informações, consulte a documentação do COM+ no SDK (Software Development Kit) do Microsoft Windows.

</dd> </dl>

## <a name="remarks"></a>Comentários

Consulte a [ação RegisterComPlus](registercomplus-action.md) e [a ação UnregisterComPlus](unregistercomplus-action.md).

Consulte [Instalando um aplicativo COM+ com o Windows Instalador do .](installing-a-com--application-with-the-windows-installer.md)

## <a name="validation"></a>Validação

<dl>

[ICE03](ice03.md)  
[ICE06](ice06.md)  
[ICE32](ice32.md)  
[ICE66](ice66.md)  
</dl>

 

 



