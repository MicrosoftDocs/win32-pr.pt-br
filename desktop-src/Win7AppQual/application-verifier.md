---
description: .
ms.assetid: edf719b7-9bd9-4e23-9bba-d0d7c3c5dbf5
title: Application Verifier (Windows 7 e Windows Server 2008 R2 Application Quality Cookbook)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dddbac00c3f16a1072a79aca096c46aaff0d2983
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103837259"
---
# <a name="application-verifier-windows-7-and-windows-server-2008-r2-application-quality-cookbook"></a>Application Verifier (Windows 7 e Windows Server 2008 R2 Application Quality Cookbook)

## <a name="affected-platforms"></a>Plataformas afetadas

**Clientes** -Windows XP Windows \| Vista Windows \| 7  
**Servidores** -windows Server 2003 \| Windows Server 2008 \| Windows Server 2008 R2  


## <a name="description"></a>Descrição

Promova e aplique Application Verifier como um portão de qualidade para todo o desenvolvimento. Ele inclui vários aprimoramentos:

-   Fornecemos verificações adicionais para resolver os problemas que a equipe de Relatório de Erros do Windows descobriu durante o uso do pool de threads.
-   Combinamos as versões de 32 e 64 bits do pacote para tratar as alterações no Windows 7, incluindo as necessidades de teste de componentes do 32-bit em uma versão de 64 bits do Windows, bem como para simplificação geral.
-   Incluímos verificações adicionais para aplicativos multissegmentados, executando aplicativos de 32 bits em Windows de 64 bits, bem como muitas correções de bugs.

Essas alterações não devem ter nenhum impacto negativo sobre os usuários que não habilitam as verificações de thread; aqueles que devem receber suporte adicional na descoberta e no diagnóstico de problemas de uso do pool de threads existentes. Independentemente de você habilitar ou não verificações de thread, você se beneficiará das outras melhorias e correções de bugs nesse serviço.

Embora haja uma ligeira penalidade de desempenho ao usar esse serviço, os níveis de desempenho devem permanecer aceitáveis porque normalmente não são executados em ambientes de varejo.

## <a name="usage"></a>Uso

**Informações Gerais**

Para fornecer aplicativos confiáveis do Windows:

1.  Aplicativos de teste escritos em código não gerenciado (nativo) com Application Verifier no depurador e com o heap de página inteira antes de liberá-lo para os clientes.
2.  Siga as etapas fornecidas pelo Application Verifier para resolver as condições de errônea.
3.  Depois que o aplicativo for liberado, monitore regularmente os relatórios de falha do aplicativo coletados pelo Relatório de Erros do Windows.

As verificações de pool de threads são habilitadas por padrão no título de verificação "Noções básicas". Como isso é incluído na configuração padrão, os usuários precisam apenas executar Application Verifier em seu código com as configurações padrão para aproveitar as novas verificações.

**Detalhes**

No mínimo, você deve executar Application Verifier com a configuração noções básicas selecionada. Isso é necessário para WinLogo e WinQual. A configuração noções básicas verifica o seguinte:

-   **Detalhes de parada de exceções** – garante que os aplicativos não ocultem violações de acesso usando manipulação de exceção estruturada
-   **Manipula os detalhes de parada** -testes para garantir que o aplicativo não esteja tentando usar identificadores inválidos
-   **Detalhes da interrupção de heaps** – verifica se há problemas de corrupção de memória no heap
-   **Detalhes de parada de entrada/saída** -monitora a execução da e/s assíncrona e executa várias validações
-   **Detalhes de parada de vazamento** -detecta vazamentos rastreando os recursos feitos por uma DLL que não são liberados quando a dll foi descarregada
-   **Detalhes da parada de bloqueios** -verifica o uso correto de seções críticas
-   **Detalhes da parada de memória** – garante que as APIs para manipulações de espaço virtual sejam usadas corretamente (por exemplo, VirtualAlloc, MapViewOfFile)
-   **Detalhes de parada de TLS** -garante que as APIs de armazenamento local de thread sejam usadas corretamente
-   **Detalhes de parada do ThreadPool** -garante o uso correto de APIs de ThreadPool e impõe verificações de consistência em Estados de thread de trabalho após um retorno de chamada

Se seu aplicativo estiver migrando de um aplicativo "pré-vista", você desejará aproveitar o "LuaPriv" (também conhecido como verificações de UAC). O LuaPriv (pregnóstico de privilégio de conta de usuário limitado) tem dois objetivos principais:

-   **Previsão**: ao executar um aplicativo com privilégio administrativo, preveja se esse aplicativo funcionaria também com menos privilégios (geralmente, como um usuário normal). Por exemplo, se o aplicativo gravar em arquivos que só permitam acesso de administradores, esse aplicativo não poderá gravar no mesmo arquivo se for executado como não administrador.
-   **Diagnóstico**: durante a execução com privilégio de não administrador, identifique possíveis problemas que já existem com a execução atual. Continuando o exemplo anterior, se o aplicativo tentar gravar em um arquivo que concede acesso somente a membros do grupo administrador, o aplicativo receberá um erro de acesso \_ negado. Se o aplicativo não funcionar corretamente, essa operação poderá ser a culpa.

LuaPriv identifica os seguintes tipos de problemas:



| **Possível problema**       | **Descrição**                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
|---------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Namespaces restritos     | Criar um objeto de sincronização nomeado (evento, semáforo, mutex, etc.) sem um namespace pode complicar a execução sem privilégios em alguns sistemas operacionais, pois o sistema operacional pode optar por posicionar o objeto em um namespace restrito. A criação de um objeto desse tipo em um namespace restrito (como o namespace global) requer SeCreateGlobalPrivilege, que é concedido somente a administradores.<br/> LuaPriv sinaliza esses dois problemas se detectar.<br/> |
| Verificações de administrador rígido | Alguns aplicativos interrogam o token de segurança do usuário para descobrir a quantidade de privilégios que ele tem. Nesses casos, o aplicativo pode alterar seu comportamento dependendo da quantidade de energia que ele acha que o usuário tem. <br/> LuaPriv sinaliza chamadas de API que retornam essas informações.<br/>                                                                                                                                                                                                |
| Solicitando privilégios     | Um aplicativo pode tentar habilitar um privilégio relevante de segurança (como SeTcbPrivilege; ou SeSecurityPrivilege) antes de executar uma operação que o exige. <br/> Os sinalizadores LuaPriv tentam habilitar os privilégios relevantes de segurança. <br/>                                                                                                                                                                                                                               |
| Privilégios ausentes        | Se um aplicativo tentar habilitar um privilégio que o usuário não tem, ele provavelmente sinalizará que o aplicativo espera o privilégio, o que pode causar diferenças de comportamento. <br/> Solicitações de privilégio com falha de sinalizadores LuaPriv. <br/>                                                                                                                                                                                                                                       |
| Operações de INI-File       | As tentativas de gravar em arquivos INI mapeados (WritePrivateProfileSection e APIs semelhantes) podem falhar como um usuário não administrador. <br/> LuaPriv sinaliza essas operações.<br/>                                                                                                                                                                                                                                                                                                            |
| Acesso negado             | Se o aplicativo tentar acessar um objeto (arquivo, chave do registro, etc.), mas a tentativa falhar devido ao acesso insuficiente, o aplicativo provavelmente espera estar em execução com mais privilégios do que ele tem. <br/> Objeto LuaPriv flags – abrir tentativas que falham com acesso \_ negado e erros semelhantes.<br/>                                                                                                                                                               |
| Negar ACEs                 | Se um objeto tiver ACEs Deny em sua DACL, ele negará explicitamente o acesso a entidades específicas. <br/> Isso é incomum e dificulta a previsão, por isso sinalizadores LuaPriv negam ACEs quando as encontra.<br/>                                                                                                                                                                                                                                                                     |
| Acesso restrito         | Se um aplicativo tentar abrir um objeto para direitos que não são concedidos a usuários normais (por exemplo, tentar gravar em um arquivo que só é gravável por administradores), o aplicativo provavelmente não funcionará da mesma forma quando executado como um usuário normal. <br/> LuaPriv sinaliza essas operações.<br/>                                                                                                                                                                      |
| MÁXIMO \_ permitido          | Se um aplicativo abrir um objeto para \_ o máximo permitido, a verificação de acesso real no objeto ocorrerá em outro lugar. A maioria dos códigos que faz isso não funciona corretamente e certamente funcionará de maneira diferente quando executado sem privilégios. <br/> O LuaPriv, portanto, sinaliza todos os incidentes do máximo \_ permitido. <br/>                                                                                                                                                            |



 

Os problemas comumente ignorados são capturados nas verificações diversas do nebulosas:

-   Detalhes de parada de APIs perigosas
-   Detalhes da interrupção das pilhas sujas
-   Substituição de tempo

Adicionamos um novo verificador de impressão. Essa camada ajuda a encontrar e solucionar problemas que podem ocorrer quando um aplicativo chama o subsistema de impressão. O verificador de impressão visa as duas camadas do subsistema de impressão, a camada PrintAPI e a camada PrintDriver.

*Camada de API de impressão*

O verificador de impressão testa a interface entre um programa e winspool. drv e prntvpt.dll e testa as interfaces dessas DLLs. Você pode examinar as regras para chamar funções nesta interface na seção de ajuda do MSDN para APIs exportadas por winspool. drv e prntvpt.dll.

*Camada do driver de impressão*

O verificador de impressão também testa a interface entre um driver de impressão principal, como UNIDRV.DLL, UNIDRUI.DLL, PSCRIPT5.DLL, PS5UI.DLL ou MXDWDRV.DLL e os plug-ins de driver de impressão. Você pode encontrar informações sobre essa interface no MSDN e no WDK.

Observe que algumas dessas verificações são apenas para o Windows 7, e outras simplesmente terão um desempenho melhor no Windows 7.

Normalmente, somente as versões de depuração executam o Application Verifier, portanto, o desempenho não é geralmente um problema. Se surgirem problemas de desempenho do uso deste ou de qualquer outra verificação de Application Verifier, execute uma verificação por vez até que você tenha realizado todas as verificações necessárias.

Quase 10% das falhas de aplicativo nos sistemas Windows são devido à corrupção de heap. Essas falhas são quase impossíveis de depurar após o fato. A melhor maneira de evitar esses problemas é testar com os recursos de heap de página encontrados em Application Verifier. Há dois tipos de heap de página: "Full" e "Light". Full é o padrão; Ele forçará um depurador a parar instantaneamente após detectar a corrupção. Esse recurso deve ser executado no depurador. No entanto, também é o mais exigente recurso. Se um usuário estiver tendo problemas de tempo e já tiver executado um cenário no heap de página "completo", configurá-lo como "Light" provavelmente resolverá esses problemas. Além disso, o heap de página leve não falha até que o processo saia. Ele fornece um rastreamento de pilha para a alocação, mas pode levar consideravelmente mais tempo para diagnosticar do que aproveitar sua contraparte completa.

Monitore o status de confiabilidade dos aplicativos por meio do portal da Web do winqual. Esse portal mostra os relatórios de erros coletados por meio do Relatório de Erros do Windows, portanto, é fácil identificar as falhas mais frequentes. Saiba mais sobre isso em Relatório de Erros do Windows: Introdução. A Microsoft não cobra por esse serviço.

Para aproveitar o WinQual, você deve:

1.  Registre sua empresa para WinQual, que requer uma ID da VeriSign. Você pode encontrar informações sobre o Windows 7 sobre o WinQual no portal do desenvolvedor agrupado em Windows Vista SP1 \\ Windows Server 2008. Ele terá um local do Windows 7 em breve.
2.  Mapeie os aplicativos ISV para um nome de produto e o nome do ISV, que vincula os relatórios de falha à empresa. Outros ISVs não podem exibir seus relatórios de erros.
3.  Use o portal para identificar os principais problemas. Os ISVs também podem criar respostas que informem aos clientes quais etapas executar após uma falha. O sistema de resposta dá suporte a mais de 10 idiomas no mundo todo.

Mais uma observação: Application Verifier é tão boa quanto os caminhos de código com os quais você o executa. O valor da combinação dessa ferramenta com uma ferramenta de cobertura de código não pode ser com um estado muito decodificado.

## <a name="links-to-other-resources"></a>Links para outros recursos

**Ferramentas de depuração para Windows:**

-   [Visão geral e site de download](https://msdn.microsoft.com/windows/hardware/bg127145)
-   [Documentação online do MSDN](/windows-hardware/drivers/debugger/)

**Application Verifier:**

-   [Visão geral](/previous-versions/ms220948(v=vs.80))
-   [Download](https://www.microsoft.com/downloads/details.aspx?FamilyID=c4a25ab9-649d-4a1b-b4a7-c9d8b095df18&amp;DisplayLang=en)
-   [Application Verifier para Microsoft Visual Studio 2008/.NET Framework 3,5](/previous-versions/ms220948(v=vs.80))

    **Observação:** a versão Application Verifier fornecida no Visual Studio é bem atualizada. Se possível, use o pacote autônomo em vez disso. Por esse motivo, as versões futuras do Visual Studio não terão mais Application Verifier inseridos.

**WinQual:**

-   [Winqual (Windows Quality Online Services)](/windows-hardware/drivers/dashboard/winqual-submission-tool--winqualexe-)
-   [Relatório de Erros do Windows: Introdução](../wer/using-wer.md)

 

 
