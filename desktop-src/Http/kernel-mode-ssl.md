---
title: SSL de modo kernel
description: SSL de modo kernel
ms.assetid: ada82704-cb7d-4e98-8c87-76c7bfbd098b
keywords:
- SSL de modo kernel
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fdfbc66e72f4e3e79c53207cbe9f4b77d3887b36
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2021
ms.locfileid: "122475492"
---
# <a name="kernel-mode-ssl"></a>SSL de modo kernel

o SSL do modo Kernel foi introduzido no Windows Server 2003 com Service Pack 1 (SP1) com suporte limitado. para computadores em execução no Windows Server 2003 com SP1, uma chave do registro deve ser definida para habilitar o SSL do kernel. para computadores que executam o Windows Server 2008 e Windows Vista, o suporte ao modo kernel completo para SSL é fornecido.

As seções a seguir descrevem o suporte a SSL do modo kernel:

-   modos de Kernel SSL no Windows Server 2003 com SP1
-   modo Kernel SSL no Windows Server 2008 e Windows Vista

## <a name="kernel-modes-ssl-in-windows-server-2003-with-sp1"></a>modos de Kernel SSL no Windows Server 2003 com SP1

no Windows Server 2003 com SP1, a API do servidor HTTP fornece a opção de executar segurança SSL no modo kernel (o modo de usuário SSL é o padrão). O recurso de modo kernel melhora o desempenho do SSL ao mover as operações de criptografia e descriptografia para o kernel, reduzindo assim o número de transições entre o modo kernel e o modo de usuário.

Os recursos a seguir não têm suporte quando o SSL é executado no modo kernel:

-   Certificados do cliente
-   Codificações RC2
-   O protocolo PCT 1,0
-   As alterações de configuração do certificado do servidor exigem uma reinicialização do serviço HTTP
-   Suporte a criptografia e descarregamento em massa

## <a name="configuring-kernel-mode-ssl"></a>Configurando o modo kernel SSL

O SSL do modo kernel é controlado pelo valor do registro **EnableKernelSSL** e é habilitado pela definição do valor como 1. Habilitar o modo kernel SSL desabilitará o modo de usuário SSL e exigirá que o serviço HTTP seja reiniciado para entrar em vigor. A chave do registro **EnableKernelSSL** está localizada em:

**HKEY \_ \_** Parâmetros http do sistema de computador local \\  \\ **CurrentControlSet** \\ **Services** \\  \\  \\ **EnableKernelSSL**

## <a name="kernel-mode-ssl-in-windows-server-2008-and-windows-vista"></a>modo Kernel SSL no Windows Server 2008 e Windows Vista

para computadores em execução no Windows Server 2008 e Windows Vista, a API do servidor HTTP apresenta a funcionalidade avançada do SSL.

Os novos recursos a seguir têm suporte:

-   Suporte completo a certificados do cliente no modo kernel SSL
-   SSL de modo kernel para todas as transações HTTP SSL
-   Suporte a criptografia e descarregamento em massa
-   O protocolo PCT 1,0
-   Codificações RC2
-   Aumento do desempenho no modo de usuário SSL

## <a name="configuration"></a>Configuração

O SSL do modo kernel é configurável por meio de dois valores de registro na chave parâmetros HTTP localizada em:

```
HKEY_LOCAL_MACHINE
   System
      CurrentControlSet
         Services
            HTTP
               Parameters
                  EnableSslCloseNotify
                  DisableSslCertChainCacheOnlyUrlRetrieval
```

Um usuário deve ter privilégios de administrador/sistema local para modificar os valores do registro e exibir, ou modificar, os arquivos de log e a pasta que os contém.

As informações de configuração nos valores do registro são lidas quando o driver da API do servidor HTTP é iniciado. Como resultado, se as configurações forem alteradas, o driver deverá ser interrompido e reiniciado para ler os novos valores. Isso pode ser feito usando os seguintes comandos de console:

**net stop http**

**net start http**

A tabela a seguir lista os valores de configuração do registro.




| Valor do registro | Descrição | 
|----------------|-------------|
| EnableKernelSSL | <strong>Windows Server 2008 e Windows Vista:</strong> Esse valor de registro é obsoleto.<br /> | 
| EnableSslCloseNotify | Um valor <strong>DWORD</strong> que é definido como <strong>true</strong> para habilitar o Close-notificar ou <strong>false</strong> para desabilitar o requisito de fechamento de notificação. O fechamento da notificação é desabilitado por padrão.<br /> Quando fechar-Notify estiver habilitado, o aplicativo cliente será solicitado a enviar uma mensagem de aviso de fechamento antes de fechar as conexões TCP. A API do servidor HTTP também envia um aviso de fechamento antes de fechar a conexão.<br /> Quando fechar-Notify estiver habilitado e o cliente enviar uma mensagem de aviso de fechamento, a API do servidor HTTP reutilizará a sessão SSL em conexões futuras com o cliente. Se o cliente não enviar um aviso de fechamento, a API do servidor HTTP não reutilizará a mesma sessão SSL em conexões futuras. Assim, um handshake SSL completo é disparado na nova conexão, reduzindo o desempenho. <br /><blockquote>[!Note]<br />Habilitar o fechamento da notificação ajuda a reduzir os ataques de truncamento em relação às solicitações e respostas HTTPS.</blockquote><br /><br /> Quando fechar-notificar está desabilitado, a API do servidor HTTP reutiliza a sessão SSL para conexões futuras.<br /> | 
| DisableSslCertChainCacheOnlyUrlRetrieval | Um valor <strong>DWORD</strong> definido como <strong>true</strong> para habilitar a API do servidor http para recuperar certificados intermediários da Internet ou do repositório local ou <strong>false</strong> para recuperar certificados intermediários somente do repositório local. O valor padrão do registro é <strong>false</strong>.<br /> Por padrão, a API do servidor HTTP cria uma cadeia de certificados de cliente recuperando os certificados intermediários do repositório de autoridade de certificação intermediária na conta do computador local. Definir esse valor como <strong>true</strong> permite que a API do servidor http recupere os certificados intermediários não apenas do armazenamento local, mas também da autoridade de certificação intermediária na Internet.<br /> | 




 

 

 





