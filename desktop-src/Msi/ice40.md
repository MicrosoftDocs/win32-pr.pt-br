---
description: ICE40 faz validação diversas.
ms.assetid: 1f2ba2a1-0170-4434-88fd-a5d1ca8b67c4
title: ICE40
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 077c44154413d9aa9e75b1c13fe2f2f80ccb52fee6459888c7bc9678ea0e935f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119528426"
---
# <a name="ice40"></a>ICE40

ICE40 faz validação diversas.

## <a name="result"></a>Resultado

O ICE40 posta avisos sobre o seguinte:

-   A [**propriedade REINSTALLMODE**](reinstallmode.md) foi substituído.
-   A [tabela RemoveIniFile tem](removeinifile-table.md) uma entrada Excluir Marca sem valor.
-   O .msi arquivo não tem a [tabela](error-table.md) Erro e a propriedade [**Resumo**](page-count-summary.md) da Contagem de Páginas é menor ou igual a 100. Esse aviso ICE está obsoleto porque Windows Instalador não exige que o pacote tenha uma tabela Error. As mensagens de erro podem ser recuperadas usando Msimsg.dll.

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



| Erro ICE40                                                                                           | Descrição                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
|-------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**REINSTALLMODE**](reinstallmode.md) é definido na tabela Property. Isso pode causar dificuldades. | Definir a [**propriedade REINSTALLMODE**](reinstallmode.md) no arquivo .msi pode levar a um comportamento inesperado. Para corrigir esse erro, não defina essa propriedade.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                 |
| A entrada RemoveIniFile Remove1 deve ter um valor, pois a Ação é "Excluir Marca" (4).                | Há uma ação Excluir Marca no na coluna RemoveIniFile da tabela [RemoveIniFile](removeinifile-table.md) sem especificar uma marca a ser excluído na coluna Valor.                                                                                                                                                                                                                                                                                                                                                                                                                         |
| A Tabela de Erros está ausente. Somente mensagens de erro numéricas serão geradas.                              | Este aviso ICE está obsoleto porque Windows Instalador não exige que o pacote tenha uma [tabela Error](error-table.md). As mensagens de erro podem ser recuperadas usando Msimsg.dll.<br/> Esse aviso significa que o arquivo .msi [](error-table.md) está ausente [](page-count-summary.md) na tabela Erro e a propriedade Resumo da Contagem de Páginas é menor ou igual a 100. <br/> Para corrigir esse erro, use uma versão atual do instalador Windows ou adicione uma tabela Error ao pacote de instalação e os modelos de formatação de autor na coluna Mensagem para mensagens de erro.<br/> |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Referência de ICE](ice-reference.md)
</dt> </dl>

 

 




