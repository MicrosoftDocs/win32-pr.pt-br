---
title: Restrições de shell gráfico do servidor
description: Os aplicativos do servidor devem ser capazes de executar sem o shell gráfico do servidor
ms.assetid: 8F531497-B64D-4E79-AD7A-790EFDC6ADFE
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ae2a3002fc2395faba3e07d90a2322c770fe3ee9
ms.sourcegitcommit: 099ecdda1e83618b844387405da0db0ebda93a65
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/04/2021
ms.locfileid: "111443217"
---
# <a name="server-apps-must-be-able-to-run-without-the-server-graphical-shell"></a>Os aplicativos do servidor devem ser capazes de executar sem o shell gráfico do servidor

## <a name="platform"></a>Plataforma

**Servidores** – Windows Server 2012 

## <a name="description"></a>Descrição

O shell gráfico do servidor, o recurso que inclui o Windows Explorer e o Internet Explorer, é instalado por padrão nas instalações "servidor com uma GUI" do Windows Server 2012. O recurso de shell gráfico do servidor pode ser desinstalado para reduzir o potencial de manutenção e de serviço, limitando assim o número de reinicializações que o servidor pode incorrer e, ao mesmo tempo, permitindo que as ferramentas de gerenciamento sejam executadas localmente no servidor.

Depois que um administrador desinstala o shell gráfico do servidor, o servidor está na configuração mínima da interface do servidor:

![configuração da interface do shell gráfico do servidor](images/minimalserverinterface.png)

Os administradores podem optar por executar na configuração mínima da interface do servidor (que inclui um conjunto de ferramentas de gerenciamento local), como o padrão, em vez de no servidor com uma configuração de GUI. Isso permite o monitoramento e o gerenciamento local, ao mesmo tempo em que reduz o uso de recursos e a frequência de manutenção.

Os administradores poderão reinstalar o shell gráfico do servidor posteriormente se precisarem da funcionalidade dentro dele. (Os administradores também podem iniciar a partir de uma instalação do Server Core e "criar" para a configuração mínima da interface do servidor usando os recursos de funcionalidade sob demanda.)

Os aplicativos de servidor devem ser capazes de executar na configuração mínima da interface do servidor para aproveitar a redução da utilização de recursos e da superfície de manutenção. Esse recurso pode ser obtido permitindo que o administrador opte por não instalar partes do aplicativo que precise do shell gráfico do servidor ou detectando a presença do shell gráfico do servidor e desabilitando alguns aspectos do aplicativo.

A interface mínima do servidor tem um espaço reduzido de recursos e manutenção, pois muitas APIs e binários incluídos no shell gráfico do servidor não estão disponíveis nessa configuração. Quando apropriado, os aplicativos de servidor também devem permitir a administração remota (preferencialmente por meio da comunicação remota do Windows PowerShell) de outra instalação do Windows Server ou do cliente Windows. Isso permite uma melhor administração centralizada de um ou mais computadores na configuração mínima da interface do servidor ou de computadores em uma configuração de superfície ainda menor, como Server Core.

## <a name="manifestation"></a>Manifestação

Se um aplicativo exigir qualquer uma das APIs ou binários que não estão disponíveis na configuração mínima da interface do servidor, ele poderá não ser exibido corretamente na tela e/ou ser inutilizável.

## <a name="mitigation"></a>Atenuação

Os desenvolvedores de aplicativos de servidor devem identificar as partes de seus aplicativos que exigem qualquer uma das APIs ou binários removidos e incluir informações para o administrador do servidor que identifica as partes do aplicativo que não serão executadas corretamente ao usar a interface de servidor mínima. Se essas partes do aplicativo puderem ser instaladas opcionalmente ou não forem absolutamente necessárias para a funcionalidade do produto, o aplicativo ainda poderá ser instalado e executado na configuração mínima da interface do servidor.

Se o aplicativo não puder ser usado sem o shell gráfico do servidor, essa limitação deverá ser documentada e o administrador do servidor deverá ser instruído a instalar o shell gráfico do servidor. (Se estiver adicionando a uma instalação do Server Core, isso pode exigir a adição de recursos usando recursos sob demanda.) Além disso, o aplicativo deve verificar a inicialização de que todos os arquivos necessários estão disponíveis, pois o shell gráfico do servidor pode ser desinstalado a qualquer momento antes ou depois da instalação do aplicativo.

## <a name="solution"></a>Solução

Conte com o menor conjunto possível de dependências e modularizate aplicativos para que a funcionalidade principal do aplicativo possa funcionar sem a necessidade de componentes de interface do usuário mais pesados instalados. Desenvolva aplicativos que não exigem nenhuma das APIs ou binários removidos e, em vez disso, conte com a funcionalidade contida na interface mínima do servidor ou Server Core. Isso reduzirá os requisitos de manutenção e melhorará o desempenho e a satisfação do usuário.

Onde há partes de um aplicativo que podem adicionar uma funcionalidade significativa quando o shell gráfico do servidor está disponível, os desenvolvedores de aplicativos podem:

-   Permitir que esses recursos adicionais usem o shell gráfico do servidor para serem instalados opcionalmente, para que possam ser omitidos das instalações em uma configuração mínima de interface do servidor
-   Detectar a presença do shell gráfico do servidor e adaptar o comportamento do aplicativo

Os desenvolvedores de aplicativos também devem garantir que os aplicativos de servidor sejam gerenciáveis remotamente quando possível e apropriados.

## <a name="detecting-minimal-server-interface-and-server-core"></a>Detectando a interface mínima do servidor e o Server Core

O Windows Server instalará um valor de registro correspondente para cada nível de servidor instalado. Você pode consultar a existência dessas chaves para determinar se o shell gráfico do servidor ou os recursos de interface mínima do servidor estão instalados e habilitados.

HKEY \_ local \_ Machine \\ software \\ Microsoft \\ Windows NT \\ CurrentVersion \\ Server \\ ServerLevels:



|   &nbsp;         | Server Core | Interface Mínima do Servidor | Shell gráfico do servidor |
|------------------|-------------|--------------------------|------------------------|
| ServerCore = 1     | X           | X                        | X                      |
| Servidor-GuiMgmt = 1 |             | X                        | X                      |
| ServerGuiShell = 1 |             |                          | X                      |



 

Um "X" na tabela acima significa que a chave do registro estará presente quando o recurso correspondente for instalado.

Observe que esses níveis de servidor são aditivos; Se o shell gráfico do servidor estiver instalado, a interface do servidor e o Server Core serão mínimos. Nesse caso, ambas as chaves do registro estarão presentes.

## <a name="tests"></a>Testes

Inspecione o código do aplicativo para obter os requisitos que usam qualquer um dos binários e APIs removidos. Depois de ter removido todas as instâncias desses binários de "principais aplicativos", teste seu aplicativo em um ambiente que não inclua o shell gráfico do servidor. Ferramentas como o Process Monitor podem ajudar com isso.

Se você não puder interromper completamente o uso dessas APIs e binários, certifique-se de que seu aplicativo falhe normalmente quando executado na interface mínima do servidor ou Server Core.

## <a name="resources"></a>Recursos

-   [Documentos do Server Core existentes no MSDN](/previous-versions/windows/desktop/legacy/ms723891(v=vs.85))

 

 