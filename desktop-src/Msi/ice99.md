---
description: ICE99 verifica se nenhum nome de propriedade inserido na tabela de diretório duplica um nome reservado para o uso público ou privado do Windows Installer.
ms.assetid: a7657c14-6542-4a7b-a8f7-727b109cfc39
title: ICE99
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 25744243ad5de8adc6a88ebc09890eb006d94e929a56e469ce802ad67f9a230b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119315266"
---
# <a name="ice99"></a>ICE99

ICE99 verifica se nenhum nome de propriedade inserido na tabela de [diretório](directory-table.md) duplica um nome reservado para o uso público ou privado do Windows Installer.

## <a name="result"></a>Resultado

ICE99 posta o erro a seguir.



| Erro de ICE99                                                                                                      | Description                                                                                                                                   |
|------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------|
| O nome do diretório: \[ 1 \] é o mesmo que uma das propriedades públicas do MSI e pode causar efeitos colaterais imprevistos. | o valor na coluna directory da tabela de [diretórios](directory-table.md) duplica um nome de propriedade reservado pelo Windows Installer. |



 

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

[sem suporte no Windows Installer 3,0 e versões anteriores](not-supported-in-windows-installer-version-3-0.md)
</dt> </dl>

 

 



