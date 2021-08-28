---
description: ICE41 valida que as entradas nas tabelas de classe e extensão se referem a entradas na tabela de componentes que implementam o objeto de classe ou a extensão do componente.
ms.assetid: 43572322-ba23-4f99-be34-e572d4c6e3eb
title: ICE41
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0c220e43cf8a275e520f5babe1ca609a1cee2194b4c08f8dcdafabe6d73bdca4
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119581106"
---
# <a name="ice41"></a>ICE41

ICE41 valida que as entradas nas tabelas de [classe](class-table.md) e [extensão](extension-table.md) se referem a entradas na [tabela de componentes](component-table.md) que implementam o objeto de classe ou a extensão do componente.

## <a name="result"></a>Resultado

ICE41 posta um erro se houver um recurso que não contém o componente que implementa a extensão ou o objeto de classe.

## <a name="example"></a>Exemplo

ICE41 relata os erros a seguir para o exemplo mostrado.



| Erro de ICE41                                                                                                                                                                                    | Descrição                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| {00000000-0000-0000-0000-0000000000000}A classe referencia o recurso Feature2 e o componente Component1, mas o componente não está associado a esse recurso na tabela FeatureComponents. | Há um recurso que não contém o componente que implementa o objeto de classe. Isso significa que o instalador não instala o componente com o recurso e que o anúncio pode não funcionar conforme o esperado. Para corrigir esse erro, altere a entrada na coluna recurso \_ da entrada da [tabela de classes](class-table.md) para fazer referência a um recurso que instala o componente listado na \_ coluna componente ou altere o recurso e o componente associados na [tabela FeatureComponents](featurecomponents-table.md).<br/>          |
| A extensão. Yip referencia o recurso Feature1 e o componente Component2, mas o componente não está associado a esse recurso na tabela FeatureComponents.                                | Há um recurso que não contém o componente que implementa a extensão. Isso significa que o instalador não instala o componente com o recurso e que o anúncio pode não funcionar conforme o esperado. Para corrigir esse erro, altere a entrada na coluna recurso \_ da entrada da [tabela de extensão](extension-table.md) para fazer referência a um recurso que instala o componente listado na \_ coluna componente ou altere o recurso e o componente associados na [tabela FeatureComponents](featurecomponents-table.md).<br/> |



 

[Tabela FeatureComponents](featurecomponents-table.md) (parcial)



| Recurso\_ |
|-----------|
| Feature1  |
| Feature2  |



 

[Tabela de classes](class-table.md) (parcial)



| CLSID                                  | Componente\_ | Recurso\_ |
|----------------------------------------|-------------|-----------|
| {00000000-0000-0000-0000-000000000000} | Component1  | Feature2  |



 

[Tabela de classes](class-table.md) (parcial)



| Extensão | Componente\_ | Recurso\_ |
|-----------|-------------|-----------|
| .yip      | Component2  | Feature1  |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Referência de ICE](ice-reference.md)
</dt> </dl>

 

 




