---
description: A tabela MsiEmbeddedUI define uma interface do usuário inserida no pacote Windows Installer.
ms.assetid: d4176f99-e819-4b5a-bd06-1a2965891f9a
title: Tabela MsiEmbeddedUI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a52846e88e2d8f3edb439aa6b4a49c99e252173f
ms.sourcegitcommit: 7b8f6151ebe247536304866459b2973276271d4d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/06/2021
ms.locfileid: "105751434"
---
# <a name="msiembeddedui-table"></a>Tabela MsiEmbeddedUI

A tabela MsiEmbeddedUI define uma interface do usuário inserida no pacote Windows Installer.

**[Windows Installer 4,0 ou anterior](not-supported-in-windows-installer-4-0.md):** Sem suporte. Esta tabela está disponível a partir do Windows Installer 4,5.

A tabela MsiEmbeddedUI tem as colunas a seguir.



| Coluna        | Tipo                               | Chave | Nullable |
|---------------|------------------------------------|-----|----------|
| MsiEmbeddedUI | [Identificador](identifier.md)       | S   | N        |
| FileName      | [Text](text.md)                   | N   | N        |
| Atributos    | [Inteiro](integer.md)             | N   | N        |
| MessageFilter | [DoubleInteger](doubleinteger.md) | N   | S        |
| Dados          | [Binary](binary.md)               | N   | N        |



 

## <a name="columns"></a>Colunas

<dl> <dt>

<span id="MsiEmbeddedUI"></span><span id="msiembeddedui"></span><span id="MSIEMBEDDEDUI"></span>MsiEmbeddedUI
</dt> <dd>

A chave primária da tabela.

</dd> <dt>

<span id="FileName"></span><span id="filename"></span><span id="FILENAME"></span>Nome do arquivo
</dt> <dd>

O nome do arquivo que recebe as informações binárias na coluna de dados. O nome do arquivo é necessário para incluir uma extensão. Por exemplo, o nome *embeddedui.dll* é aceitável, mas *embeddedui* é inaceitável. O nome pode ser localizado. Esse campo pode conter um nome de arquivo curto ou um nome de arquivo longo, mas não pode conter ambos. O formato desse campo é como o tipo de dados de coluna [filename](filename.md) , exceto que o separador de barra vertical ( \| ) para a sintaxe de nome curto de arquivo/nome de arquivo longo não está disponível. Como alguns servidores Web podem diferenciar maiúsculas de minúsculas, o nome de arquivo deve corresponder ao caso dos arquivos de origem exatamente para garantir o suporte a downloads da Internet.

</dd> <dt>

<span id="Attributes"></span><span id="attributes"></span><span id="ATTRIBUTES"></span>Atributos
</dt> <dd>

Informações sobre os dados na coluna de dados. O valor neste campo pode conter uma ou mais das constantes a seguir.



| Constante                      | Hexadecimal | Decimal | Significado                                                                                                                                                                                                                          |
|-------------------------------|-------------|---------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Nenhum                          | 0x00        | 0       | O arquivo não é o arquivo DLL para a interface do usuário. Pode ser um arquivo de recurso usado pela interface do usuário.                                                                                                                       |
| **msidbEmbeddedUI**           | 0x01        | 1       | O arquivo DLL primário para a interface do usuário. Não é possível marcar mais de uma linha na tabela com este atributo. Se várias linhas forem marcadas com esse atributo, será um erro e não será possível garantir que a DLL seja usada. |
| **msidbEmbeddedHandlesBasic** | 0x02        | 2       | Permite que o instalador invoque a interface do usuário inserida durante uma instalação básica no nível da interface do usuário. O instalador ignora esse atributo se ele não estiver combinado com o atributo **msidbEmbeddedUI** .                                         |



 

</dd> <dt>

<span id="MessageFilter"></span><span id="messagefilter"></span><span id="MESSAGEFILTER"></span>MessageFilter
</dt> <dd>

Especifica os tipos de mensagens que são enviadas para a DLL da interface do usuário. Essa coluna só é relevante para linhas com o atributo **msidbEmbeddedUI** . Esse campo deverá ser nulo se uma linha fizer referência a um arquivo de recurso e o valor de atributos for nulo. Se uma linha fizer referência a uma DLL de interface do usuário, o valor dessa coluna não deverá ser nulo.

O valor nessa coluna pode ser uma combinação dos valores a seguir. O instalador ignora todos os outros valores.



| Constante                           | Hexadecimal | Decimal   | Descrição                                                                                                  |
|------------------------------------|-------------|-----------|--------------------------------------------------------------------------------------------------------------|
| **INSTALLLOGMODE \_ FATALEXIT**      | 0x00001     | 1         | Encerramento prematuro.                                                                                       |
| **erro de INSTALLLOGMODE \_**          | 0x00002     | 2         | Mensagens de erro.                                                                                              |
| **aviso de INSTALLLOGMODE \_**        | 0x00004     | 4         | Mensagens de aviso.                                                                                            |
| **\_usuário INSTALLLOGMODE**           | 0x00008     | 8         | Mensagens do usuário.                                                                                               |
| **informações de INSTALLLOGMODE \_**           | 0x00010     | 16        | Mensagens de status não registradas.                                                                                    |
| **INSTALLLOGMODE \_ FILESINUSE**     | 0x00020     | 32        | Arquivos atualmente mantidos em uso.                                                                                 |
| **INSTALLLOGMODE \_ resolver**  | 0x00040     | 64        | Solicitações de resolução de origem.                                                                                  |
| **INSTALLLOGMODE \_ OUTOFDISKSPACE** | 0x00080     | 128       | Mensagens de espaço em disco.                                                                                         |
| **INSTALLLOGMODE \_ ACTIONSTART**    | 0x00100     | 256       | Mensagens de início de ação.                                                                                       |
| **INSTALLLOGMODE \_ ACTIONDATA**     | 0x00200     | 512       | Mensagens de dados de ação.                                                                                        |
| **progresso do INSTALLLOGMODE \_**       | 0x00400     | 1024      | Mensagens de progresso.                                                                                           |
| **INSTALLLOGMODE \_ COMMONDATA**     | 0x00800     | 2.048      | Mensagens de inicialização da interface do usuário.                                                                                  |
| **INSTALLLOGMODE \_ inicializar**     | 0x01000     | 4096      | Mensagens de inicialização da interface do usuário enviadas quando uma instalação do produto é iniciada.                                            |
| **INSTALLLOGMODE \_ encerrar**      | 0x02000     | 8192      | Mensagens de desligamento da interface do usuário enviadas após a conclusão de uma instalação do produto.                                         |
| **INSTALLLOGMODE \_ SHOWDIALOG**     | 0x04000     | 16384     | Mensagens enviadas antes da exibição da caixa de diálogo da interface do usuário.                                                             |
| **INSTALLLOGMODE \_ RMFILESINUSE**   | 0x02000000  | 33554432  | Arquivos atualmente mantidos em uso.                                                                                 |
| **INSTALLLOGMODE \_ INSTALLSTART**   | 0x04000000  | 67108864  | A instalação do produto começa. A mensagem contém o NomeDoProduto e o ProductCode do produto.              |
| **INSTALLLOGMODE \_ INSTALLEND**     | 0x08000000  | 134217728 | A instalação do produto termina. A mensagem contém o NomeDoProduto, o ProductCode e o valor de retorno do produto. |



 

</dd> <dt>

<span id="Data"></span><span id="data"></span><span id="DATA"></span>Dado
</dt> <dd>

Esta coluna contém informações binárias. Se o campo de atributo estiver marcado com o atributo **msidbEmbeddedUI** , as informações nesse campo deverão ser uma dll. Se o campo de atributo não for o atributo **msidbEmbeddedUI** , as informações nesse campo poderão ser um arquivo de recurso em qualquer formato.

</dd> </dl>

## <a name="remarks"></a>Comentários

Para usar uma interface de usuário inserida, o desenvolvedor da instalação deve criar essa funcionalidade no pacote de Windows Installer. A tabela MsiEmbeddedUI define a interface do usuário inserida. A DLL para a interface do usuário inserida deve exportar as funções *InitializeEmbeddedUI*, *EmbeddedUIHandler* e *ShutdownEmbeddedUI* . Os pacotes que não dão suporte a uma interface de usuário inserida podem usar a interface do usuário interna do Windows Installer.

Para executar as [ferramentas de depuração para Windows](https://www.microsoft.com/?ref=go) em uma interface de usuário inserida, use as técnicas descritas em [Depurando ações personalizadas](debugging-custom-actions.md). Defina o valor de MsiBreak como MsiEmbeddedUI.

Para obter um exemplo de uma interface do usuário personalizada inserida, consulte [usando uma interface do usuário inserida](using-an-embedded-ui.md).

 

 



