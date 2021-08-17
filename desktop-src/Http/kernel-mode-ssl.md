---
title: SSL do modo kernel
description: SSL do modo kernel
ms.assetid: ada82704-cb7d-4e98-8c87-76c7bfbd098b
keywords:
- SSL do modo kernel
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3c9dcfeb87b1a98539d7bd6a3b8b82dcfd5ee41fc9ad4c4c306f4c399aebd18a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118393914"
---
# <a name="kernel-mode-ssl"></a>SSL do modo kernel

O modo kernel SSL foi introduzido no Windows Server 2003 com Service Pack 1 (SP1) com suporte limitado. Para computadores em execução no Windows Server 2003 com SP1, uma chave do Registro deve ser definida para habilitar o kernel SSL. Para computadores em execução no Windows Server 2008 e Windows Vista, é fornecido suporte completo ao modo kernel para SSL.

As seções a seguir descrevem o suporte a SSL do modo kernel:

-   Kernel Modes SSL no Windows Server 2003 com SP1
-   Modo kernel SSL no Windows Server 2008 e Windows Vista

## <a name="kernel-modes-ssl-in-windows-server-2003-with-sp1"></a>Kernel Modes SSL no Windows Server 2003 com SP1

No Windows Server 2003 com SP1, a API do Servidor HTTP fornece a opção de executar a segurança SSL no modo kernel (o SSL do modo de usuário é o padrão). O recurso de modo kernel melhora o desempenho de SSL movendo operações de criptografia e descriptografia para o kernel, reduzindo assim o número de transições entre o modo kernel e o modo de usuário.

Não há suporte para os seguintes recursos quando o SSL é executado no modo kernel:

-   Certificados do cliente
-   Codificações RC2
-   O protocolo PCT 1.0
-   As alterações na configuração do certificado do servidor exigem uma reinicialização do serviço HTTP
-   Suporte à criptografia e descarregador em massa

## <a name="configuring-kernel-mode-ssl"></a>Configurando o SSL do modo kernel

O modo kernel SSL é controlado pelo valor do Registro **EnableKernelSSL** e é habilitado definindo o valor como 1. A habilitação do modo kernel SSL desabilitará o modo de usuário SSL e exigirá que o serviço HTTP seja reiniciado para que entre em vigor. A **chave do Registro EnableKernelSSL** está localizada em:

**HKEY \_ \_Parâmetros** \\  \\ HTTP \\  \\  \\  \\ **enableKernelSSL** do sistema LOCAL MACHINE CurrentControlSet Services

## <a name="kernel-mode-ssl-in-windows-server-2008-and-windows-vista"></a>Modo kernel SSL no Windows Server 2008 e Windows Vista

Para computadores em execução Windows Server 2008 e Windows Vista, a API do servidor HTTP apresenta funcionalidade SSL aprimorada.

Há suporte para os seguintes novos recursos:

-   Suporte completo ao certificado do cliente no modo kernel SSL
-   Modo kernel SSL para todas as transações HTTP SSL
-   Suporte à criptografia e descarregador em massa
-   O protocolo PCT 1.0
-   Codificações RC2
-   Maior desempenho em relação ao modo de usuário SSL

## <a name="configuration"></a>Configuração

O modo kernel SSL é configurável por meio de dois valores do Registro na chave Parâmetros HTTP localizada em:

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

Um usuário deve ter privilégios de Administrador/Sistema Local para modificar os valores do Registro e exibir ou modificar os arquivos de log e a pasta que os contém.

As informações de configuração nos valores do Registro são lidas quando o driver de API do servidor HTTP é iniciado. Como resultado, se as configurações são alteradas, o driver deve ser interrompido e reiniciado para ler os novos valores. Isso pode ser feito usando os seguintes comandos de console:

**net stop http**

**net start http**

A tabela a seguir lista os valores de configuração do Registro.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Valor do Registro</th>
<th>Descrição</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>EnableKernelSSL</td>
<td><strong>Windows Server 2008 e Windows Vista:</strong> Esse valor do Registro está obsoleto.<br/></td>
</tr>
<tr class="even">
<td>EnableSslCloseNotify</td>
<td>Um <strong>valor DWORD</strong> definido como <strong>TRUE</strong> para habilitar a notificação de fechamento ou <strong>FALSE</strong> para desabilitar o requisito de notificação de fechamento. A notificação de fechamento está desabilitada por padrão.<br/> Quando a notificação de fechamento está habilitada, o aplicativo cliente é necessário para enviar uma mensagem close-notify antes de fechar conexões TCP. A API do Servidor HTTP também envia uma notificação de fechamento antes de fechar a conexão.<br/> Quando a notificação de fechamento estiver habilitada e o cliente enviar uma mensagem de notificação próxima, a API do Servidor HTTP reutilizará a sessão SSL em conexões futuras com o cliente. Se o cliente não enviar uma notificação próxima, a API do Servidor HTTP não reutilizará a mesma sessão SSL em conexões futuras. Portanto, um handshake SSL completo é disparado na nova conexão, reduzindo assim o desempenho. <br/>
<blockquote>
[!Note]<br />
A habilitação da notificação de fechamento ajuda a atenuar ataques de truncamento contra as solicitações e respostas HTTPS.
</blockquote>
<br/> <br/> Quando a notificação de fechamento é desabilitada, a API do Servidor HTTP reutiliza a sessão SSL para conexões futuras.<br/></td>
</tr>
<tr class="odd">
<td>DisableSslCertChainCacheOnlyUrlRetrieval</td>
<td>Um <strong>valor DWORD</strong> definido como <strong>TRUE</strong> para permitir que a API do Servidor HTTP recupere certificados intermediários da Internet ou do armazenamento local ou <strong>FALSE</strong> para recuperar certificados intermediários somente do armazenamento local. O valor padrão do Registro é <strong>FALSE.</strong><br/> Por padrão, a API do Servidor HTTP cria uma cadeia de certificados do cliente recuperando os certificados intermediários do armazenamento da Autoridade de Certificação Intermediária na conta do computador local. Definir esse valor como <strong>TRUE</strong> permite que a API do Servidor HTTP recupere os certificados intermediários não apenas do armazenamento local, mas também da Autoridade de Certificação Intermediária na Internet.<br/></td>
</tr>
</tbody>
</table>



 

 

 





