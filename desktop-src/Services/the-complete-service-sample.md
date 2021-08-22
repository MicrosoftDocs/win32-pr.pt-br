---
description: 'Saiba mais sobre: O exemplo de serviço completo'
ms.assetid: a3aeea9b-09c0-4834-892a-c378b67402f4
title: O exemplo de serviço completo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a1f3f5fc0fb59342841a9d1f1280475ace12c54998d59e5f36a19557f0ccc5c3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118888327"
---
# <a name="the-complete-service-sample"></a>O exemplo de serviço completo

Os tópicos nesta seção formam um exemplo de serviço completo:

-   [Sample.mc](sample-mc.md) (contém mensagens de erro)
-   [Svc.cpp](svc-cpp.md) (contém o código de serviço)
-   [SvcConfig.cpp (contém](svcconfig-cpp.md) código de configuração de serviço)
-   [SvcControl.cpp](svccontrol-cpp.md) (contém o código de controle de serviço)

## <a name="building-the-service"></a>Criando o serviço

O procedimento a seguir descreve como criar o serviço e registrar a DLL da mensagem de evento.

**Para criar o serviço e registrar a DLL da mensagem de evento**

1.  Crie a DLL de mensagem Sample.mc usando as seguintes etapas:
    1.  **mc -U sample.mc**
    2.  **rc -r sample.rc**
    3.  **link -dll -noentry -out:sample.dll sample.res**
2.  Crie Svc.exe, SvcConfig.exe e SvcControl.exe de Svc.cpp, SvcConfig.cpp e SvcControl.cpp, respectivamente.
3.  Crie a chave do Registro **HKEY \_ LOCAL MACHINE SYSTEM \_ \\ \\ CurrentControlSet \\ Services \\ EventLog Application \\ \\ SvcName** e adicione os seguintes valores de Registro a essa chave.

    | Valor                              | Tipo       | Descrição                                                                                                        |
    |------------------------------------|------------|--------------------------------------------------------------------------------------------------------------------|
    | **EventMessageFile**  =  *caminho \_ dll* | REG \_ SZ    | O caminho para a DLL somente recurso que contém cadeias de caracteres que o serviço pode gravar no log de eventos.               |
    | **TypesSupported** = 0x00000007    | REG \_ DWORD | Uma máscara de bits que especifica os tipos de evento com suporte. O valor 0x000000007 indica que todos os tipos têm suporte. |

    

     

## <a name="testing-the-service"></a>Testando o serviço

O procedimento a seguir descreve como testar o serviço.

**Para testar o serviço**

1.  Em Painel de Controle, inicie o **aplicativo Serviços.** (Nas etapas a seguir, use a tecla F5 para atualizar a exibição depois de executar um comando que modifica as informações no **aplicativo Serviços.)**
2.  Execute o seguinte comando para instalar o serviço:

    **instalação do svc**

    O serviço grava "Serviço instalado com êxito" no console se a operação for bem-sucedida ou uma mensagem de erro caso contrário.

    Se a instalação do serviço for bem-sucedida, o serviço será exibido no **aplicativo Serviços.** Observe que Nome **está** definido como "SvcName",  Descrição e **Status** estão em branco e Tipo de Inicialização está definido como "Manual". 

3.  Execute o seguinte comando para iniciar o serviço:

    **svccontrol start SvcName**

    Se a operação for bem-sucedida, o programa de controle de serviço escreverá "Início do serviço pendente..." e , em seguida, "O serviço foi iniciado com êxito" no console. Caso contrário, o programa grava uma mensagem de erro no console.

    Se o serviço for iniciado com êxito, **Status** será definido como "Iniciado". O código na [*função ServiceMain*](/windows/win32/api/winsvc/nc-winsvc-lpservice_main_functiona) é executado pelo SCM. Se ocorrer um erro, o serviço gravará uma mensagem de erro no log de eventos. Essa mensagem inclui o nome da função que falhou e o código de erro retornado em caso de falha.

4.  Execute o seguinte comando para atualizar a descrição do serviço:

    **svcconfig describe SvcName**

    O programa de configuração de serviço grava "Descrição do serviço atualizada com êxito" no console se a operação for bem-sucedida ou uma mensagem de erro caso contrário.

    Se a atualização for bem-sucedida, **Descrição** será definida como "Esta é uma descrição de teste".

5.  Execute o seguinte comando para consultar a configuração do serviço:

    **Svcconfig query SvcName**

    O programa de configuração de serviço grava as informações de configuração de serviço no console se a operação for bem-sucedida ou uma mensagem de erro caso contrário.

6.  Execute o seguinte comando para alterar a DACL de serviço:

    **svccontrol dacl SvcName**

    O programa de configuração de serviço grava "DACL de serviço atualizada com êxito" no console se a operação for bem-sucedida ou uma mensagem de erro caso contrário.

7.  Execute o seguinte comando para desabilitar o serviço:

    **svcconfig disable SvcName**

    O programa de configuração de serviço grava "Serviço desabilitado com êxito" no console se a operação for bem-sucedida ou uma mensagem de erro caso contrário.

    Se o serviço for desabilitado com êxito, **o Tipo de Inicialização** será definido como "Desabilitado".

8.  Execute o seguinte comando para habilitar o serviço:

    **svcconfig enable SvcName**

    O programa de configuração de serviço grava "Serviço habilitado com êxito" no console se a operação for bem-sucedida ou uma mensagem de erro caso contrário.

    Se o serviço estiver habilitado com êxito, o **Tipo de Inicialização** será definido como "Manual".

9.  Execute o seguinte comando para interromper o serviço:

    **svccontrol stop SvcName**

    Se a operação for bem-sucedida, o programa de controle de serviço escreverá "Parada de serviço pendente..." e , em seguida, "Serviço interrompido com êxito" no console. Caso contrário, o programa grava uma mensagem de erro no console.

    Se o serviço for interrompido com êxito, **o Status** será em branco.

    Se o serviço não conseguir parar, o programa de controle de serviço grava uma mensagem de erro no log de eventos que inclui o nome da função que falhou e o código de erro retornado em caso de falha.

10. Execute o seguinte comando para excluir o serviço:

    **svcconfig delete SvcName**

    O programa de configuração de serviço grava "Serviço excluído com êxito" no console se a operação for bem-sucedida ou uma mensagem de erro caso contrário.

    Se o serviço for excluído com êxito, ele não será mais exibido no **aplicativo Serviços.** (Observe que, se você tentar excluir um serviço que  não foi interrompido, a operação será bem-sucedida, mas o Tipo de Inicialização será definido como "Desabilitado" e a entrada de serviço será excluída na reinicialização do sistema ou quando o serviço for encerrado usando Gerenciador de Tarefas.)

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Usando serviços](using-services.md)
</dt> </dl>

 

 
