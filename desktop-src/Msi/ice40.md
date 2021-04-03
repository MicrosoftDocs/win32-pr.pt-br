---
description: ICE40 faz uma validação diversas.
ms.assetid: 1f2ba2a1-0170-4434-88fd-a5d1ca8b67c4
title: ICE40
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 17617fe5748fcba5ae0edab414ad1bc83c2e5c22
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104091732"
---
# <a name="ice40"></a>ICE40

ICE40 faz uma validação diversas.

## <a name="result"></a>Resultado

O ICE40 posta avisos sobre o seguinte:

-   A propriedade [**REinstallmode**](reinstallmode.md) foi substituída.
-   A [tabela RemoveIniFile](removeinifile-table.md) tem uma entrada Delete tag sem valor.
-   O arquivo. msi não tem a [tabela de erros](error-table.md) e a propriedade de [**Resumo de contagem de páginas**](page-count-summary.md) é menor ou igual a 100. Este aviso de gelo está obsoleto porque Windows Installer não exige que o pacote tenha uma tabela de erro. As mensagens de erro podem ser recuperadas usando Msimsg.dll.

## <a name="example"></a>Exemplo

[Tabela de propriedades](property-table.md)



| Propriedade                               | Valor |
|----------------------------------------|-------|
| [**REINSTALLMODE**](reinstallmode.md) | Um     |



 

[Tabela RemoveIniFile](removeinifile-table.md)



| RemoveIniFile                          | Ação | Valor |
|----------------------------------------|--------|-------|
| [**REINSTALLMODE**](reinstallmode.md) | 4      |       |



 

## <a name="results"></a>Resultados

ICE40 relataria os erros a seguir.



| Erro de ICE40                                                                                           | Descrição                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
|-------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**REinstallmode**](reinstallmode.md) é definido na tabela de propriedades. Isso pode causar dificuldades. | Definir a propriedade [**REinstallmode**](reinstallmode.md) no arquivo. msi pode levar a um comportamento inesperado. Para corrigir esse erro, não defina essa propriedade.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                 |
| A entrada RemoveIniFile Remove1 deve ter um valor, pois a ação é "excluir marca" (4).                | Há uma ação DELETE tag no na coluna RemoveIniFile da [tabela RemoveIniFile](removeinifile-table.md) sem especificar uma marca a ser excluída na coluna Value.                                                                                                                                                                                                                                                                                                                                                                                                                         |
| A tabela de erros está ausente. Serão geradas apenas mensagens de erro numéricas.                              | Este aviso de gelo está obsoleto porque Windows Installer não exige que o pacote tenha uma [tabela de erro](error-table.md). As mensagens de erro podem ser recuperadas usando Msimsg.dll.<br/> Esse aviso significa que o arquivo. msi não tem a [tabela de erros](error-table.md) e a propriedade de [**Resumo de contagem de páginas**](page-count-summary.md) é menor ou igual a 100. <br/> Para corrigir esse erro, use uma versão atual do Windows Installer ou adicione uma tabela de erros ao pacote de instalação e crie modelos de formatação na coluna mensagem para mensagens de erro.<br/> |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Referência de ICE](ice-reference.md)
</dt> </dl>

 

 




