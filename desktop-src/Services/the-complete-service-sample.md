---
description: 'Saiba mais sobre: o exemplo de serviço completo'
ms.assetid: a3aeea9b-09c0-4834-892a-c378b67402f4
title: O exemplo de serviço completo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eb87ebfef3f964eacee66be94a4b5291c335d0d5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105754494"
---
# <a name="the-complete-service-sample"></a>O exemplo de serviço completo

Os tópicos nesta seção formam um exemplo de serviço completo:

-   [Sample.MC](sample-mc.md) (contém mensagens de erro)
-   [Svc. cpp](svc-cpp.md) (contém o código de serviço)
-   [SvcConfig. cpp](svcconfig-cpp.md) (contém o código de configuração de serviço)
-   [SvcControl. cpp](svccontrol-cpp.md) (contém código de controle de serviço)

## <a name="building-the-service"></a>Criando o serviço

O procedimento a seguir descreve como criar o serviço e registrar a DLL de mensagem de evento.

**Para compilar o serviço e registrar a DLL de mensagem de evento**

1.  Crie a DLL de mensagem do Sample.mc usando as seguintes etapas:
    1.  **MC-U sample.mc**
    2.  **RC-r Sample. rc**
    3.  **link-dll-NOENTRY -out:sample.dll amostra. res**
2.  Crie Svc.exe, SvcConfig.exe e SvcControl.exe de svc. cpp, SvcConfig. cpp e SvcControl. cpp, respectivamente.
3.  Crie a chave do registro **HKEY \_ local \_ Machine \\ System \\ CurrentControlSet \\ Services \\ EventLog \\ Application \\ SvcName** e adicione os seguintes valores de registro a essa chave.

    | Valor                              | Tipo       | Descrição                                                                                                        |
    |------------------------------------|------------|--------------------------------------------------------------------------------------------------------------------|
    | **EventMessageFile**  =  *\_ caminho da dll* | REG \_ sz    | O caminho para a DLL somente de recursos que contém cadeias de caracteres que o serviço pode gravar no log de eventos.               |
    | **TypesSupported** = 0x00000007    | REG \_ DWORD | Uma máscara de bits que especifica os tipos de eventos com suporte. O valor 0x000000007 indica que todos os tipos têm suporte. |

    

     

## <a name="testing-the-service"></a>Testando o serviço

O procedimento a seguir descreve como testar o serviço do.

**Para testar o serviço**

1.  No painel de controle, inicie o aplicativo **Serviços** . (Nas etapas a seguir, use a tecla F5 para atualizar a exibição depois de executar um comando que modifica as informações no aplicativo de **Serviços** .)
2.  Execute o seguinte comando para instalar o serviço:

    **instalação do SVC**

    O serviço grava "serviço instalado com êxito" no console do se a operação for bem-sucedida ou uma mensagem de erro de outra forma.

    Se a instalação do serviço for realizada com sucesso, o serviço será exibido no aplicativo **Serviços** . Observe que **Name** está definido como "SvcName", a **Descrição** e o **status** estão em branco e o **tipo de inicialização** é definido como "manual".

3.  Execute o seguinte comando para iniciar o serviço:

    **svccontrol iniciar SvcName**

    Se a operação for concluída com sucesso, o programa de controle de serviço gravará "início do serviço pendente..." e "o serviço foi iniciado com êxito" no console do. Caso contrário, o programa gravará uma mensagem de erro no console.

    Se o serviço for iniciado com êxito, o **status** será definido como "iniciado". O código na função de [*immain*](/windows/win32/api/winsvc/nc-winsvc-lpservice_main_functiona) é executado pelo SCM. Se ocorrer um erro, o serviço gravará uma mensagem de erro no log de eventos. Essa mensagem inclui o nome da função que falhou e o código de erro que foi retornado em caso de falha.

4.  Execute o seguinte comando para atualizar a descrição do serviço:

    **svcconfig descrever SvcName**

    O programa de configuração de serviço grava "Descrição do serviço atualizada com êxito" no console do se a operação for bem-sucedida ou uma mensagem de erro de outra forma.

    Se a atualização for realizada com sucesso, a **Descrição** será definida como "esta é uma descrição de teste".

5.  Execute o seguinte comando para consultar a configuração do serviço:

    **svcconfig consulta SvcName**

    O programa de configuração de serviço grava as informações de configuração do serviço no console do se a operação for concluída com sucesso ou uma mensagem de erro de outra forma.

6.  Execute o seguinte comando para alterar a DACL do serviço:

    **svccontrol DACL SvcName**

    O programa de configuração de serviço grava o "serviço DACL atualizado com êxito" no console do se a operação for bem-sucedida ou uma mensagem de erro de outra forma.

7.  Execute o seguinte comando para desabilitar o serviço:

    **svcconfig desabilitar SvcName**

    O programa de configuração de serviço grava "serviço desabilitado com êxito" no console do se a operação for bem-sucedida ou uma mensagem de erro caso contrário.

    Se o serviço for desabilitado com êxito, o **tipo de inicialização** será definido como "desabilitado".

8.  Execute o seguinte comando para habilitar o serviço:

    **svcconfig habilitar SvcName**

    O programa de configuração de serviço grava "serviço habilitado com êxito" no console do se a operação for bem-sucedida ou uma mensagem de erro de outra forma.

    Se o serviço for habilitado com êxito, o **tipo de inicialização** será definido como "manual".

9.  Execute o seguinte comando para interromper o serviço:

    **svccontrol parar SvcName**

    Se a operação for concluída com sucesso, o programa de controle de serviço gravará "serviço interrompido pendente..." e "o serviço foi interrompido com êxito" para o console. Caso contrário, o programa gravará uma mensagem de erro no console.

    Se o serviço for interrompido com êxito, o **status** será em branco.

    Se o serviço não for interrompido, o programa de controle de serviço gravará uma mensagem de erro no log de eventos que inclui o nome da função que falhou e o código de erro que foi retornado em caso de falha.

10. Execute o seguinte comando para excluir o serviço:

    **svcconfig excluir SvcName**

    O programa de configuração de serviço grava "serviço excluído com êxito" no console do se a operação for bem-sucedida ou uma mensagem de erro de outra forma.

    Se o serviço for excluído com êxito, ele não será mais exibido no aplicativo de **Serviços** . (Observe que se você tentar excluir um serviço que não está parado, a operação terá sucesso, mas o **tipo de inicialização** será definido como "desabilitado" e a entrada de serviço será excluída na reinicialização do sistema ou quando o serviço for encerrado usando o Gerenciador de tarefas.)

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Usando serviços](using-services.md)
</dt> </dl>

 

 
