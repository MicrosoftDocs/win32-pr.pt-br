---
description: O ICE38 valida que cada componente que está sendo instalado no perfil do usuário atual também especifica uma chave do Registro na raiz HKEY CURRENT USER na coluna KeyPath da tabela \_ \_ Componente.
ms.assetid: f1548b04-78c2-461a-a729-9a8c4856d0d8
title: ICE38
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2ae3f90b7f6c0624da266b23dee3a50489f34604d6c99783b337eeca77bb32ca
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119528456"
---
# <a name="ice38"></a>ICE38

O ICE38 valida que todos os componentes que estão sendo instalados no perfil do usuário atual também especificam uma chave do Registro na raiz **HKEY \_ CURRENT \_ USER** na coluna KeyPath da tabela [Componente](component-table.md).

## <a name="result"></a>Resultado

ICE38 postará um erro se um componente instalado no perfil do usuário não especificar uma chave do Registro HKCU.

## <a name="example"></a>Exemplo

ICE38 relata os seguintes erros para o exemplo mostrado.



| Erro ICE38                                                                                                                         | Descrição                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
|-------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Component Component1 é instalado no perfil do usuário. Ele deve usar uma chave do Registro em HKCU como seu KeyPath, não um arquivo.                    | O valor da coluna de atributos de Component1 é 0, o que significa que o componente deve usar um arquivo como seu KeyPath. Isso causa dificuldades quando vários usuários instalam o componente no mesmo computador. Para corrigir esse erro no Component1, de definido o bit [](component-table.md) RegistryKeyPath na coluna Atributos da tabela Componente e altere a entrada na coluna KeyPath para um valor listado na coluna Registro da tabela registro [.](registry-table.md)<br/>                                                                                |
| Component Component2 é instalado no perfil do usuário. Ele deve usar uma chave do Registro em HKCU como seu KeyPath. O KeyPath atualmente é NULL. | Component2 tem o bit RegistryKeyPath definido na coluna Atributos da [tabela Componente](component-table.md). Portanto, o campo KeyPath deve conter uma chave para a coluna Registro da Tabela do [Registro,](registry-table.md) mas a coluna KeyPath é Null. Para corrigir esse erro, altere o valor KeyPath para uma entrada válida na tabela Registro.<br/>                                                                                                                                                                                                     |
| Component Component3 é instalado no perfil do usuário. A chave do Registro KeyPath deve se enquadrar em HKCU.                                      | Component3 tem o bit RegistryKeyPath definido [](component-table.md) na coluna Atributos da tabela Componente, mas a raiz da entrada do Registro especificada na coluna Raiz da tabela registro especifica **HKEY \_ LOCAL \_ MACHINE** em vez de **HKEY \_ CURRENT \_ USER**. Para corrigir esse erro, use uma entrada de Registro válida em **HKEY \_ LOCAL \_ MACHINE** como KeyPath para esse componente ou altere o valor na coluna Raiz da tabela Registro para -1 ou 1. [](registry-table.md)<br/>                                                                  |
| A entrada do Registro KeyPath para o componente Component4 não existe.                                                                 | Component4 tem o bit RegistryKeyPath definido [](component-table.md) na coluna Atributos da tabela Componente, mas a entrada na coluna KeyPath não existe na Tabela [do Registro](registry-table.md). Para corrigir esse erro, adicione uma entrada para Reg4 à tabela registro que é um em **HKEY \_ CURRENT \_ USER**.<br/>                                                                                                                                                                                                                                      |
| A Entrada do Registro Reg5 é definida como KeyPath para o componente Component5, mas essa entrada do Registro não pertence ao Component5.      | A entrada do Registro referenciada na coluna KeyPath do componente foi encontrada e está na árvore HKCU, mas a coluna Componente da entrada do Registro não se refere ao mesmo componente que o listou como \_ KeyPath. Isso significa que a entrada do Registro usada como KeyPath do componente só seria criada quando algum outro componente fosse instalado. Para corrigir esse erro, altere o valor keyPath para se referir a uma entrada do Registro que pertence ao componente ou altere a entrada do Registro para pertencer ao componente usando-o como um KeyPath.<br/> |



 

[Tabela de diretórios](directory-table.md) (parcial)



| Diretório | Pai do \_ Diretório | Defaultdir      |
|-----------|-------------------|-----------------|
| Dir1      |                   | StartMenuFolder |
| Dir2      |                   | DesktopFolder   |
| Dir3      | Dir3              | AppData         |
| Dir4      | Dir3              | Subdir          |



 

[Tabela de componentes](component-table.md) (parcial)



| Componente  | Diretório\_ | Atributos | KeyPath |
|------------|-------------|------------|---------|
| Component1 | Dir1        | 0          | Arquivo1   |
| Component2 | Dir2        | 4          |         |
| Component3 | Dir3        | 4          | Reg3    |
| Component4 | Dir4        | 4          | Reg4    |
| Component5 | Dir5        | 4          | Reg5    |



 

[Tabela do Registro](registry-table.md) (parcial)



| Registro | Root | Valor | Componente\_ |
|----------|------|-------|-------------|
| Reg3     | 2    |       | Component3  |
| Reg5     | 0    |       | Component4  |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Referência de ICE](ice-reference.md)
</dt> </dl>

 

 




