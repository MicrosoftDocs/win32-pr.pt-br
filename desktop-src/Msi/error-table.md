---
description: A tabela de erros é usada para pesquisar modelos de formatação de mensagem de erro ao processar erros com um código de erro definido, mas sem um conjunto de modelos de formatação (essa é a situação normal).
ms.assetid: 3c817468-cba7-46bf-9208-5e6699c02fb6
title: Tabela de erros
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5cfcba5f68eb48621891c7a48aeedea2329996f6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104169858"
---
# <a name="error-table"></a>Tabela de erros

A tabela de erros é usada para pesquisar modelos de formatação de mensagem de erro ao processar erros com um código de erro definido, mas sem um conjunto de modelos de formatação (essa é a situação normal).

A tabela de erros tem as colunas a seguir.



| Coluna  | Tipo                     | Chave | Nullable |
|---------|--------------------------|-----|----------|
| Erro   | [Inteiro](integer.md)   | S   | N        |
| Mensagem | [Modelo](template.md) | N   | S        |



 

## <a name="columns"></a>Colunas

<dl> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>Ao
</dt> <dd>

Consulte [Windows Installer mensagens de erro](windows-installer-error-messages.md) para obter uma lista de números de erro e mensagens.

O número do erro deve ser um inteiro não negativo.

O intervalo de 25000 a 30000 é reservado para erros de ações personalizadas. Os autores de ações personalizadas podem usar esse intervalo para suas ações personalizadas.

</dd> <dt>

<span id="Message"></span><span id="message"></span><span id="MESSAGE"></span>Mensagem
</dt> <dd>

Esta coluna contém o modelo de formatação de erro localizável. A tabela de erros é gerada pelo processo de compilação inicial para conter os modelos de formato de depuração.

A tabela a seguir lista as mensagens reservadas. Para obter uma lista de códigos de erro interno e de envio, consulte [Windows Installer mensagens de erro](windows-installer-error-messages.md).



| Erro | Mensagem                                                    | Comentários                                                                                                                                                                                                      |
|-------|------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 0     | {{Erro fatal:}}                                          | Prefixo de cabeçalho para erros fatais (INSTALLMESSAGE \_ FATALEXIT). O texto entre chaves {{Text}} só está visível no arquivo de log. O texto não é exibido para o usuário na interface de usuário.                  |
| 1     | Erro \[ 1 \] .                                               | Prefixo de cabeçalho para erros ( \_ erro INSTALLMESSAGE)                                                                                                                                                             |
| 2     | Aviso \[ 1 \] .                                             | Prefixo do cabeçalho para avisos ( \_ aviso de INSTALLMESSAGE)                                                                                                                                                         |
| 3     |                                                            |                                                                                                                                                                                                              |
| 4     | Informações \[ 1 \] .                                                | Prefixo do cabeçalho para mensagens informativas (INSTALLMESSAGE \_ info)                                                                                                                                              |
| 5     | Erro interno \[ 1 \] . \[2 \] {, \[ 3 \] } {, \[ 4 \] }              | Prefixo de cabeçalho para erros internos                                                                                                                                                                            |
| 6     |                                                            |                                                                                                                                                                                                              |
| 7     | {{Disco cheio:}}                                            | Prefixo de cabeçalho para erros de espaço em disco insuficientes (INSTALLMESSAGE \_ OUTOFDISKSPACE). O texto entre chaves {{Text}} só está visível no arquivo de log. O texto não é exibido para o usuário na interface de usuário. |
| 8     | Tempo de ação \[ \] : \[ 1 \] . \[2\]                              |                                                                                                                                                                                                              |
| 9     | \[ProductName\]                                            |                                                                                                                                                                                                              |
| 10    | { \[ 2 \] } {, \[ 3 \] } {, \[ 4 \] }                                  |                                                                                                                                                                                                              |
| 11    | Tipo de mensagem: \[ 1 \] , argumento: \[ 2\]                       |                                                                                                                                                                                                              |
| 12    | = = = Log iniciado: \[ data e \] \[ hora\] ===                 |                                                                                                                                                                                                              |
| 13    | = = = Registro em log interrompido: \[ data e \] \[ hora\] ===                 |                                                                                                                                                                                                              |
| 14    | Hora de início da ação \[ \] : \[ 1\]                               |                                                                                                                                                                                                              |
| 15    | Hora de término da ação \[ \] : \[ 1 \] . Valor de retorno \[ 2\]           |                                                                                                                                                                                                              |
| 16    | Tempo restante: { \[ 1 \] min} { \[ 2 \] seg}                    |                                                                                                                                                                                                              |
| 17    | Sem memória. Desligar outros aplicativos antes de tentar novamente |                                                                                                                                                                                                              |
| 18    | O instalador não está mais respondendo                          |                                                                                                                                                                                                              |
| 19    | Instalador encerrado prematuramente                           |                                                                                                                                                                                                              |
| 20    | Aguarde enquanto o Windows configura o \[ ProductName \] ...    |                                                                                                                                                                                                              |
| 21    | Coletando informações necessárias...                          |                                                                                                                                                                                                              |
| 22    | Removendo versões mais antigas deste aplicativo...             |                                                                                                                                                                                                              |
| 23    | Preparando para remover versões mais antigas deste aplicativo...  |                                                                                                                                                                                                              |
| 32    | \[A instalação do {ProductName \] } foi concluída com êxito.            |                                                                                                                                                                                                              |
| 33    | \[ \] Falha na instalação do {ProductName}.                            |                                                                                                                                                                                                              |



 

</dd> </dl>

## <a name="remarks"></a>Comentários

O modelo não inclui formatação para o número do erro no campo 1. Ao processar o erro, o instalador anexa um prefixo de cabeçalho ao modelo, dependendo do tipo de mensagem. Esses cabeçalhos também são armazenados na tabela de erros.

O texto entre chaves {{Text}} só está visível no arquivo de log. O texto não é exibido para o usuário na interface de usuário.

Você pode importar uma tabela de erros localizada para seu banco de dados usando Msidb.exe ou [**MsiDatabaseImport**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabaseimporta). O SDK inclui uma tabela de erros localizada para cada um dos idiomas listados na seção [localizando as tabelas Error e ActionText](localizing-the-error-and-actiontext-tables.md) . Se a tabela de erros não for populada, o instalador carregará cadeias de caracteres localizadas para o idioma especificado pela propriedade [**ProductLanguage**](productlanguage.md) .

## <a name="validation"></a>Validação

<dl>

[ICE03](ice03.md)  
[ICE06](ice06.md)  
[ICE40](ice40.md)  
[ICE46](ice46.md)  
</dl>

 

 



