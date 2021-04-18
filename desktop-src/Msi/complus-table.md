---
description: A tabela ComPlus contém as informações necessárias para instalar aplicativos COM+.
ms.assetid: 0c9a7469-5959-45ad-b84d-6cfd3e169ff6
title: Tabela ComPlus
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0a2ad5b7b96044025b78bfc774ee0767c2756aa8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105751862"
---
# <a name="complus-table"></a>Tabela ComPlus

A tabela ComPlus contém as informações necessárias para instalar aplicativos COM+.

A tabela ComPlus tem as colunas a seguir.



| Coluna      | Tipo                         | Chave | Nullable |
|-------------|------------------------------|-----|----------|
| Componente\_ | [Identificador](identifier.md) | S   | N        |
| ExpType     | [Inteiro](integer.md)       | N   | S        |



 

## <a name="columns"></a>Colunas

<dl> <dt>

<span id="Component_"></span><span id="component_"></span><span id="COMPONENT_"></span>Componente\_
</dt> <dd>

Uma chave externa na primeira coluna da tabela de [componentes](component-table.md). Esse é o componente que contém o aplicativo COM+.

</dd> <dt>

<span id="ExpType"></span><span id="exptype"></span><span id="EXPTYPE"></span>ExpType
</dt> <dd>

Sinalizadores de exportação usados durante a geração do arquivo. msi. Para obter mais informações, consulte a documentação COM+ no SDK (Software Development Kit) do Microsoft Windows.

</dd> </dl>

## <a name="remarks"></a>Comentários

Consulte a ação [RegisterComPlus](registercomplus-action.md) e a [ação UnregisterComPlus](unregistercomplus-action.md).

Consulte [instalando um aplicativo com+ com o Windows Installer](installing-a-com--application-with-the-windows-installer.md).

## <a name="validation"></a>Validação

<dl>

[ICE03](ice03.md)  
[ICE06](ice06.md)  
[ICE32](ice32.md)  
[ICE66](ice66.md)  
</dl>

 

 



