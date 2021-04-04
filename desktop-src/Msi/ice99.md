---
description: ICE99 verifica se nenhum nome de propriedade inserido na tabela de diretório duplica um nome reservado para o uso público ou privado do Windows Installer.
ms.assetid: a7657c14-6542-4a7b-a8f7-727b109cfc39
title: ICE99
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f7d70aeaf6480e45db5b47f76434f93e49adf317
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103662335"
---
# <a name="ice99"></a>ICE99

ICE99 verifica se nenhum nome de propriedade inserido na tabela de [diretório](directory-table.md) duplica um nome reservado para o uso público ou privado do Windows Installer.

## <a name="result"></a>Resultado

ICE99 posta o erro a seguir.



| Erro de ICE99                                                                                                      | Descrição                                                                                                                                   |
|------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------|
| O nome do diretório: \[ 1 \] é o mesmo que uma das propriedades públicas do MSI e pode causar efeitos colaterais imprevistos. | O valor na coluna Directory da tabela de [diretórios](directory-table.md) duplica um nome de propriedade reservado pelo Windows Installer. |



 

## <a name="example"></a>Exemplo

ICE99 relata o seguinte erro para o exemplo:

``` syntax
CustomActionData is the same as one of the MSI Public Properties and can cause unforeseen side effects.
```

[Diretório](directory-table.md) (parcial)



| Diretório        | Pai do diretório \_ | DefaultDir |
|------------------|-------------------|------------|
| CustomActionData |                   |            |



 

Para corrigir esse aviso, você deve alterar o nome de CustomActionData.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Referência de ICE](ice-reference.md)
</dt> <dt>

[Tabela de diretórios](directory-table.md)
</dt> <dt>

[Sem suporte no Windows Installer 3,0 e versões anteriores](not-supported-in-windows-installer-version-3-0.md)
</dt> </dl>

 

 



