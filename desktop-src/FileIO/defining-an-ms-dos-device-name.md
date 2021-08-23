---
description: Um nome de dispositivo MS-DOS é uma junção que aponta para o caminho de um dispositivo MS-DOS. Essas junções comem o namespace do dispositivo MS-DOS.
ms.assetid: 7d802e9f-dc09-4e3d-b064-e9b57af396e2
title: Definindo um nome de dispositivo MS-DOS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 77331c1d3b3cc7566f118fa19fbb13c84e82af634f1098193bdf3dcb6270ef7d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119638926"
---
# <a name="defining-an-ms-dos-device-name"></a>Definindo um nome de dispositivo MS-DOS

Um nome de dispositivo MS-DOS é uma junção que aponta para o caminho de um dispositivo MS-DOS. Essas junções comem o namespace do dispositivo MS-DOS. Chame as [**funções DefineDosDevice**](/windows/desktop/api/FileAPI/nf-fileapi-definedosdevicew) [**e SetVolumeMountPoint**](/windows/desktop/api/WinBase/nf-winbase-setvolumemountpointa) para criar e modificar essas junções. [**DeleteVolumeMountPoint**](/windows/desktop/api/FileAPI/nf-fileapi-deletevolumemountpointw) exclui uma junção criada por **SetVolumeMountPoint** e **DefineDosDevice** exclui junções criadas por ele.

Depois que um nome de dispositivo MS-DOS é definido, ele permanece visível para todos os processos.

-   Todos os dispositivos MS-DOS são identificados por Windows por meio de uma ID de autenticação. Uma ID de autenticação é o LUID (identificador local exclusivo) associado a cada sessão de logon quando criado.
-   A visibilidade de um nome de dispositivo MS-DOS é categorizada como global ou local e é definida como tal por sua inclusão nos namespaces de Dispositivo MS-DOS Global e Local do Dispositivo MS-DOS. O conteúdo dos dispositivos MS-DOS no namespace Global pode ser acessado por todos os usuários e o conteúdo dos dispositivos MS-DOS no namespace Local pode ser acessado somente pelo usuário cujo token de acesso contém a AuthenticationID associada a esse namespace de dispositivo MS-DOS local.

Vários namespaces de dispositivo local do MS-DOS e apenas um namespace global do dispositivo MS-DOS podem existir ao mesmo tempo e em um computador.

Observe que somente os processos em execução no contexto LocalSystem podem chamar [**DefineDosDevice**](/windows/desktop/api/FileAPI/nf-fileapi-definedosdevicew) para criar um dispositivo MS-DOS no namespace do dispositivo MS-DOS Global. Além disso, o namespace do dispositivo MS-DOS local correspondente a uma AuthenticationID específica é excluído quando a última referência a essa AuthenticationID é removida.

Quando o código consulta um nome de dispositivo MS-DOS existente chamando [**QueryDosDevice**](/windows/desktop/api/FileAPI/nf-fileapi-querydosdevicew), ele pesquisa primeiro o namespace do Dispositivo MS-DOS Local. Se ele não for encontrado lá, a função pesquisa o namespace Global do Dispositivo MS-DOS. Quando o código consulta todos os nomes de dispositivo MS-DOS existentes por meio dessa função, a lista de nomes retornados depende de se ele está em execução no contexto LocalSystem. Nesse caso, somente os nomes de dispositivo MS-DOS incluídos no namespace Global do Dispositivo MS-DOS serão retornados. Caso não seja, uma concatenação dos nomes de dispositivo nos namespaces De dispositivo MS-DOS Global e Local será retornada. Se existir um nome de dispositivo em ambos os namespaces, **QueryDosDevice** retornará a entrada no namespace Dispositivo MS-DOS Local. Isso também se aplica à lista de todos os nomes de dispositivo MS-DOS retornados por [**GetLogicalDrives**](/windows/desktop/api/FileAPI/nf-fileapi-getlogicaldrives) e [**GetLogicalDriveStrings.**](/windows/desktop/api/FileAPI/nf-fileapi-getlogicaldrivestringsw)

Observe que o seguinte cenário pode ocorrer:

1.  O usuário A, que não está em execução no contexto LocalSystem, cria um nome de dispositivo no namespace do Dispositivo MS-DOS Local correspondente e esse nome de dispositivo não existe no namespace Global do Dispositivo MS-DOS.
2.  O usuário B, que está em execução dentro do contexto LocalSystem, cria o mesmo nome de dispositivo no namespace Do dispositivo MS-DOS Global.

Nesse cenário, o Usuário A não terá acesso ao nome do dispositivo no namespace Global do Dispositivo MS-DOS até que ele remova ou renomeie o nome do dispositivo em seu namespace do Dispositivo MS-DOS Local. Para reduzir a probabilidade desse cenário ocorrer, as letras da unidade MS-DOS devem ser alocadas no namespace Do dispositivo MS-DOS Global começando com C: e terminando com Z:. Essa sequência deve ser revertida para a alocação de letras de unidade MS-DOS no namespace Do dispositivo MS-DOS local.

Se você não estiver executando no contexto LocalSystem, [**DefineDosDevice**](/windows/desktop/api/FileAPI/nf-fileapi-definedosdevicew) não permitirá que você defina um nome de dispositivo no namespace Do dispositivo MS-DOS Local se esse nome de dispositivo já existir nos namespaces do Dispositivo MS-DOS Local ou Global. Chame [**QueryDosDevice**](/windows/desktop/api/FileAPI/nf-fileapi-querydosdevicew) antes de chamar **DefineDosDevice** para determinar se o nome do dispositivo que você pretende definir existe nos namespaces do dispositivo MS-DOS.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Nomeando arquivos, caminhos e namespaces](naming-a-file.md)
</dt> </dl>

 

 



