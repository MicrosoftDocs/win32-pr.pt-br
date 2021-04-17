---
description: Um nome de dispositivo MS-DOS é uma junção que aponta para o caminho de um dispositivo MS-DOS. Essas junções compõem o namespace do dispositivo MS-DOS.
ms.assetid: 7d802e9f-dc09-4e3d-b064-e9b57af396e2
title: Definindo um nome de dispositivo MS-DOS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7ed89e1d9938e320ecce3ff0b35b8ae0792fe219
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105812959"
---
# <a name="defining-an-ms-dos-device-name"></a>Definindo um nome de dispositivo MS-DOS

Um nome de dispositivo MS-DOS é uma junção que aponta para o caminho de um dispositivo MS-DOS. Essas junções compõem o namespace do dispositivo MS-DOS. Chame as funções [**DefineDosDevice**](/windows/desktop/api/FileAPI/nf-fileapi-definedosdevicew) e [**SetVolumeMountPoint**](/windows/desktop/api/WinBase/nf-winbase-setvolumemountpointa) para criar e modificar essas junções. [**DeleteVolumeMountPoint**](/windows/desktop/api/FileAPI/nf-fileapi-deletevolumemountpointw) exclui uma junção criada por **SetVolumeMountPoint** e **DefineDosDevice** exclui as junções que ele cria.

Depois que um nome de dispositivo MS-DOS é definido, ele permanece visível para todos os processos.

-   Todos os dispositivos MS-DOS são identificados pelo Windows por meio de uma ID de autenticação. Uma ID de autenticação é a LUID (identificador local exclusivo) associada a cada sessão de logon quando criada.
-   A visibilidade de um nome de dispositivo MS-DOS é categorizada como global ou local e é definida como tal por sua inclusão nos namespaces globais do dispositivo MS-DOS e do dispositivo MS-DOS local. O conteúdo de dispositivos MS-DOS no namespace global pode ser acessado por todos os usuários, e o conteúdo de dispositivos MS-DOS no namespace local pode ser acessado somente pelo usuário cujo token de acesso contém a Authenticationid associada ao namespace do dispositivo MS-DOS local.

Vários namespaces de dispositivo do MS-DOS local e somente um namespace de dispositivo MS-DOS global podem existir ao mesmo tempo e em um computador.

Observe que somente os processos em execução no contexto LocalSystem podem chamar [**DefineDosDevice**](/windows/desktop/api/FileAPI/nf-fileapi-definedosdevicew) para criar um dispositivo MS-dos no namespace global do dispositivo MS-dos. Além disso, o namespace do dispositivo MS-DOS local correspondente a uma Authenticationid específica é excluído quando a última referência a esse Authenticationid é removida.

Quando o código consulta um nome de dispositivo MS-DOS existente chamando [**QueryDosDevice**](/windows/desktop/api/FileAPI/nf-fileapi-querydosdevicew), ele primeiro pesquisa o namespace do dispositivo MS-dos local. Se não for encontrado lá, a função pesquisará o namespace de dispositivo MS-DOS global. Quando o código consulta todos os nomes de dispositivo MS-DOS existentes por meio dessa função, a lista de nomes retornados depende de se ele está em execução no contexto LocalSystem. Nesse caso, somente os nomes de dispositivo MS-DOS incluídos no namespace de dispositivo MS-DOS global serão retornados. Caso contrário, uma concatenação dos nomes de dispositivo nos namespaces de dispositivo MS-DOS global e local será retornada. Se existir um nome de dispositivo em ambos os namespaces, **QueryDosDevice** retornará a entrada no namespace do dispositivo MS-dos local. Isso também se aplica à lista de todos os nomes de dispositivo MS-DOS retornados por [**GetLogicalDrives**](/windows/desktop/api/FileAPI/nf-fileapi-getlogicaldrives) e [**GetLogicalDriveStrings**](/windows/desktop/api/FileAPI/nf-fileapi-getlogicaldrivestringsw).

Observe que o cenário a seguir pode ocorrer:

1.  O usuário A, que não está sendo executado no contexto LocalSystem, cria um nome de dispositivo no namespace de dispositivo do MS-DOS local correspondente e esse nome de dispositivo não existe no namespace de dispositivo MS-DOS global.
2.  O usuário B, que está executando no contexto LocalSystem, cria o mesmo nome de dispositivo no namespace de dispositivo MS-DOS global.

Nesse cenário, o usuário A não terá acesso ao nome do dispositivo no namespace do dispositivo MS-DOS global até que ele remova ou renomeie o nome do dispositivo em seu namespace de dispositivo MS-DOS local. Para reduzir a probabilidade de ocorrer esse cenário, as letras de unidade do MS-DOS devem ser alocadas no namespace de dispositivo MS-DOS global, começando com C: e terminando com Z:. Essa sequência deve ser revertida para a alocação de letras de unidade do MS-DOS no namespace do dispositivo MS-DOS local.

Se você não estiver executando no contexto LocalSystem, o [**DefineDosDevice**](/windows/desktop/api/FileAPI/nf-fileapi-definedosdevicew) não permitirá que você defina um nome de dispositivo no namespace do dispositivo MS-dos local se esse nome de dispositivo já existir em seus namespaces de dispositivo MS-dos local ou global. Chame [**QueryDosDevice**](/windows/desktop/api/FileAPI/nf-fileapi-querydosdevicew) antes de chamar **DefineDosDevice** para determinar se o nome do dispositivo que você pretende definir existe em seus namespaces de dispositivo do MS-dos.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Nomeando arquivos, caminhos e namespaces](naming-a-file.md)
</dt> </dl>

 

 



