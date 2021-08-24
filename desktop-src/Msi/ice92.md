---
description: ICE92 verifica se um componente sem um GUID de ID de componente também não é especificado como um componente permanente.
ms.assetid: 5fe8a844-3f96-4b19-baa6-24e2405aff30
title: ICE92
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fd96126f9255303bb2d78f39bc6fef4312859533d1298b9a9d30afd1b79575fe
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119894876"
---
# <a name="ice92"></a>ICE92

ICE92 verifica se um componente sem um GUID de ID de componente também não é especificado como um componente permanente. Essa ação personalizada [](component-table.md) ICE verifica a Tabela de Componentes para componentes sem um [GUID](guid.md) especificado no campo ComponentId e verifica se o sinalizador **msidbComponentAttributesPermanent** não foi definido no campo Atributos. ICE92 também verifica se nenhum componente tem os atributos **msidbComponentAttributesPermanent** e **msidbComponentAttributesUninstallOnSupersedence.**

Se a coluna ComponentId for nula, o instalador não registrará o componente e o componente não poderá ser removido ou reparado pelo instalador.

## <a name="result"></a>Resultado

ICE92 posta o erro a seguir.



| Erro ICE92                                                          | Descrição                                                                                                                                                    |
|----------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| O componente ' \[ 1 \] ' não tem ComponentId e está marcado como permanente. | A entrada para esse componente na tabela Componente tem nulo na coluna ComponentId e tem **msidbComponentAttributesPermanent** na coluna Atributos. |



 

ICE92 posta o aviso a seguir.



| Aviso ICE92                                                                                                                                                           | Descrição                                                                                                                                                                                                 |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| O componente ' \[ 1 \] ' é marcado como permanente e desinstalação na supersedência. O atributo uninstall-on-supersedence será ignorado porque o componente é permanente. | A entrada para esse componente na tabela [Component](component-table.md) tem os atributos **msidbComponentAttributesPermanent** e **msidbComponentAttributesUninstallOnSupersedence especificados.** |



 

## <a name="example"></a>Exemplo

ICE92 relata o seguinte erro para o exemplo:

``` syntax
The Component 'Component1' has no ComponentId and is marked as permanent.
```

[Tabela de componentes](component-table.md) (parcial)



| Componente  | Componentid | Diretório\_ | Atributos | KeyPath |
|------------|-------------|-------------|------------|---------|
| Component1 |             | DirectoryA  | 16         | FileA   |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Referência de ICE](ice-reference.md)
</dt> </dl>

 

 



