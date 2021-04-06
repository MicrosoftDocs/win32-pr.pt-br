---
description: ICE38 valida que cada componente que está sendo instalado no perfil do usuário atual também especifica uma chave do registro na \_ raiz do usuário atual da hKey \_ na coluna KeyPath da tabela de componentes.
ms.assetid: f1548b04-78c2-461a-a729-9a8c4856d0d8
title: ICE38
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2d001d244160f939a73e697e677bf43a1f5f825f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104011295"
---
# <a name="ice38"></a>ICE38

ICE38 valida que cada componente que está sendo instalado no perfil do usuário atual também especifica uma chave do registro na raiz do **\_ \_ usuário atual da hKey** na coluna KeyPath da [tabela de componentes](component-table.md).

## <a name="result"></a>Resultado

ICE38 posta um erro se um componente instalado no perfil do usuário não especificar uma chave do Registro HKCU.

## <a name="example"></a>Exemplo

ICE38 relata os erros a seguir para o exemplo mostrado.



| Erro de ICE38                                                                                                                         | Descrição                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
|-------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| O componente Component1 é instalado no perfil do usuário. Ele deve usar uma chave do registro em HKCU como seu caminho Key, não um arquivo.                    | O valor da coluna Attributes de Component1 é 0, o que significa que o componente deve usar um arquivo como seu caminho KeyPath. Isso causa dificuldades quando vários usuários instalam o componente no mesmo computador. Para corrigir esse erro em Component1, defina o bit RegistryKeyPath na coluna Attributes da [tabela Component](component-table.md) e altere a entrada na coluna KeyPath para um valor listado na coluna Registry da [tabela Registry](registry-table.md).<br/>                                                                                |
| O componente Component2 é instalado no perfil do usuário. Ele deve usar uma chave do registro em HKCU como seu caminho de chave. O caminho keyé nulo no momento. | Component2 tem o conjunto de bits RegistryKeyPath na coluna atributos da [tabela de componentes](component-table.md). O campo KeyPath deve, portanto, conter uma chave para a coluna Registry da [tabela do registro](registry-table.md) , mas a coluna KeyPath é NULL. Para corrigir esse erro, altere o valor do caminho-chave para uma entrada válida na tabela do registro.<br/>                                                                                                                                                                                                     |
| O componente Component3 é instalado no perfil do usuário. É a chave do registro KeyPath deve estar sob HKCU.                                      | Component3 tem o conjunto de bits RegistryKeyPath na coluna atributos da [tabela de componentes](component-table.md) , mas a raiz da entrada do Registro especificada na coluna raiz da tabela do Registro especifica **HKEY \_ \_ Machine local** em vez de **HKEY \_ Current \_ User**. Para corrigir esse erro, use uma entrada de registro válida em **HKEY \_ local \_ Machine** como o caminho de chave para esse componente ou altere o valor na coluna raiz da [tabela de registro](registry-table.md) para-1 ou 1.<br/>                                                                  |
| A entrada do registro KeyPath para o componente Component4 não existe.                                                                 | Component4 tem o conjunto de bits RegistryKeyPath na coluna atributos da [tabela de componentes](component-table.md) , mas a entrada na coluna KeyPath não existe na tabela de [registro](registry-table.md). Para corrigir esse erro, adicione uma entrada para Reg4 à tabela de registro que seja em **HKEY \_ Current \_ User**.<br/>                                                                                                                                                                                                                                      |
| A entrada de registro Reg5 é definida como o caminho de chave para o componente Component5, mas essa entrada de registro não pertence a Component5.      | A entrada do registro referenciada na coluna KeyPath do componente foi encontrada e está sob a árvore HKCU, mas a coluna de componente da entrada do registro \_ não se refere ao mesmo componente que a listou como o caminho-chave. Isso significa que a entrada do Registro usada como o caminho de chave do componente só seria criada quando algum outro componente foi instalado. Para corrigir esse erro, altere o valor do caminho-chave para referir-se a uma entrada do registro que pertence ao componente ou altere a entrada do registro para pertencer ao componente usando-o como um caminho-chave.<br/> |



 

[Tabela de diretórios](directory-table.md) (parcial)



| Diretório | Pai do diretório \_ | DefaultDir      |
|-----------|-------------------|-----------------|
| Dir1      |                   | StartMenuFolder |
| Dir2      |                   | DesktopFolder   |
| Dir3      | Dir3              | AppData         |
| Dir4      | Dir3              | SubDir          |



 

[Tabela de componentes](component-table.md) (parcial)



| Componente  | Diretório\_ | Atributos | KeyPath |
|------------|-------------|------------|---------|
| Component1 | Dir1        | 0          | Arquivo1   |
| Component2 | Dir2        | 4          |         |
| Component3 | Dir3        | 4          | Reg3    |
| Component4 | Dir4        | 4          | Reg4    |
| Component5 | Dir5        | 4          | Reg5    |



 

[Tabela do registro](registry-table.md) (parcial)



| Registro | Root | Valor | Componente\_ |
|----------|------|-------|-------------|
| Reg3     | 2    |       | Component3  |
| Reg5     | 0    |       | Component4  |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Referência de ICE](ice-reference.md)
</dt> </dl>

 

 




