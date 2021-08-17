---
description: O ICE43 valida que os atalhos que não fazem referência a um recurso como seu destino (atalhos não anunciados) estão em componentes que têm uma entrada de Registro HKCU como seu caminho de chave.
ms.assetid: 7e58e303-e512-4707-a0bf-2095ec8ec502
title: ICE43
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c69af661b22d851b50a74bdffb9534b1e269dde4e428440882ee2d52813a68c7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118635202"
---
# <a name="ice43"></a>ICE43

O ICE43 valida que os atalhos que não fazem referência a um recurso como seu destino (atalhos não anunciados) estão em componentes que têm uma entrada de Registro HKCU como seu caminho de chave.

## <a name="result"></a>Resultado

ICE43 posta uma mensagem de erro se um atalho não anunciado estiver em um componente que não tem uma entrada de Registro HKCU como seu caminho de chave.

## <a name="example"></a>Exemplo

ICE43 relataria os erros a seguir para o exemplo mostrado.



| Erro de ICE43                                                                                                                             | Descrição                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
|-----------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| O componente Component1 tem atalhos não anunciados. Ele deve usar uma chave do registro em HKCU como seu caminho Key, não um arquivo.                    | A coluna Attributes de Component1 é 0, o que significa que o componente usa um arquivo como seu caminho KeyPath. Isso faz com que atalhos não anunciados neste componente sejam instalados somente para o primeiro usuário no computador. Os usuários que instalarem o componente mais tarde não verão os atalhos porque o componente aparece para o instalador já existente no computador. Para corrigir esse erro, defina o bit RegistryKeyPath dos atributos para alternar o componente para uma entrada de registro e, em seguida, altere o valor de caminho Keypara uma entrada válida na tabela do registro.<br/> |
| O componente Component2 tem atalhos não anunciados. Ele deve usar uma chave do registro em HKCU como seu caminho de chave. O caminho keyé nulo no momento. | A coluna atributos está definida para usar o registro, mas o caminho keyé nulo. O caminho de chave deve se referir a uma entrada na tabela do registro. Para corrigir esse erro, altere o valor do caminho-chave para uma entrada válida na tabela do registro.<br/>                                                                                                                                                                                                                                                                                                                               |
| O componente Component3 tem atalhos não anunciados. Sua chave do registro KeyPath deve estar sob HKCU.                                       | A coluna atributos é definida para usar o registro, mas a entrada de registro referenciada não está sob HKCU. Para corrigir esse erro, alterne para uma entrada de registro diferente como o caminho de chave para esse componente ou altere o valor raiz da entrada do registro para-1 ou 1.<br/>                                                                                                                                                                                                                                                                             |
| A entrada do registro KeyPath para o componente Component4 não existe.                                                                     | A entrada do registro referenciada na coluna KeyPath do componente não está na tabela do registro. Para corrigir esse erro, crie uma entrada.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                 |
| A entrada de registro Reg5 é definida como o caminho de chave para o componente Component5, mas essa entrada de registro não pertence a Component5.          | Há uma entrada de registro referenciada na coluna KeyPath do componente que está sob a árvore HKCU, mas a coluna de componente da entrada do registro \_ não se refere ao mesmo componente que a listou como o caminho-chave. Isso significa que a entrada do Registro usada como o caminho de chave do componente só será criada se algum outro componente tiver sido instalado. Para corrigir esse erro, altere o valor do caminho-chave para referir-se a uma entrada do registro que pertence ao componente ou altere a entrada do registro para pertencer ao componente usando-o como um caminho-chave.<br/>   |



 

[Tabela de componentes](component-table.md) (parcial)



| Componente  | Atributos | KeyPath |
|------------|------------|---------|
| Component1 | 0          | Arquivo1   |
| Component2 | 4          |         |
| Component3 | 4          | Reg3    |
| Component4 | 4          | Reg4    |
| Component5 | 4          | Reg5    |



 

[Tabela do registro](registry-table.md) (parcial)



| Registro | Root | Valor | Componente\_ |
|----------|------|-------|-------------|
| Reg3     | 2    |       | Component3  |
| Reg5     | 0    |       | Component4  |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Referência de ICE](ice-reference.md)
</dt> </dl>

 

 




