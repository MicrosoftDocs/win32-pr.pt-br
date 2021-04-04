---
description: ICE92 verifica se um componente sem um GUID de ID de componente também não foi especificado como um componente permanente.
ms.assetid: 5fe8a844-3f96-4b19-baa6-24e2405aff30
title: ICE92
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 63c9cffdfd7ac30313ed24182d8b4cc94f25900f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103828874"
---
# <a name="ice92"></a>ICE92

ICE92 verifica se um componente sem um GUID de ID de componente também não foi especificado como um componente permanente. Essa ação personalizada de ICE verifica a tabela de componentes em busca de [componente](component-table.md) sem um [GUID](guid.md) especificado no campo ComponentID e verifica se o sinalizador **msidbComponentAttributesPermanent** não foi definido no campo atributos. ICE92 também verifica se nenhum componente tem os atributos **msidbComponentAttributesPermanent** e **msidbComponentAttributesUninstallOnSupersedence** .

Se a coluna ComponentID for nula, o instalador não registrará o componente e o componente não poderá ser removido ou reparado pelo instalador.

## <a name="result"></a>Resultado

ICE92 posta o erro a seguir.



| Erro de ICE92                                                          | Descrição                                                                                                                                                    |
|----------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| O componente ' \[ 1 \] ' não tem ComponentID e está marcado como permanente. | A entrada deste componente na tabela de componentes tem nulo na coluna ComponentID e tem **msidbComponentAttributesPermanent** na coluna atributos. |



 

ICE92 posta o aviso a seguir.



| Aviso de ICE92                                                                                                                                                           | Descrição                                                                                                                                                                                                 |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| O componente ' \[ 1 \] ' está marcado como permanente e como desinstalar-on-substituition. O atributo Uninstall-on-substituition será ignorado porque o componente é permanente. | A entrada para esse componente na [tabela de componentes](component-table.md) tem os atributos **msidbComponentAttributesPermanent** e **msidbComponentAttributesUninstallOnSupersedence** especificados. |



 

## <a name="example"></a>Exemplo

ICE92 relata o seguinte erro para o exemplo:

``` syntax
The Component 'Component1' has no ComponentId and is marked as permanent.
```

[Tabela de componentes](component-table.md) (parcial)



| Componente  | ComponentId | Diretório\_ | Atributos | KeyPath |
|------------|-------------|-------------|------------|---------|
| Component1 |             | Directorya  | 16         | FileA   |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Referência de ICE](ice-reference.md)
</dt> </dl>

 

 



