---
description: O Schannel retorna as seguintes mensagens de erro quando o alerta correspondente é recebido dos protocolos TLS ou protocolo SSL (segurança da camada de transporte).
ms.assetid: 0a6ac61d-a00c-4fc8-a995-d25d17e405df
title: Códigos de erro Schannel para alertas TLS e SSL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4819c39948a2baf5889734fe7e2c08c8d85cbd22868cc9fad8a33281d13a306c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118918585"
---
# <a name="schannel-error-codes-for-tls-and-ssl-alerts"></a>Códigos de erro Schannel para alertas TLS e SSL

O [*Schannel*](../secgloss/s-gly.md) retorna as seguintes mensagens de erro quando o alerta correspondente é recebido dos protocolos TLS ou [*protocolo SSL*](../secgloss/s-gly.md) (segurança da [*camada de transporte*](../secgloss/t-gly.md) ). As mensagens de erro são definidas em Winerror. h.



| Alerta de TLS ou SSL                                           | Código de erro Schannel                                                   |
|------------------------------------------------------------|-----------------------------------------------------------------------|
| \_ \_ Mensagem inesperada de alerta do SSL3 \_<br/> 10<br/>  | \_mensagem s E \_ inválida \_<br/> 0x80090326<br/>             |
| \_Mac de \_ registro insatisfatório de alerta \_ de TLS1 \_<br/> 20<br/>     | s \_ E \_ mensagem \_ alterada<br/> 0x8009030F<br/>             |
| \_ \_ Falha na descriptografia de alerta TLS1 \_<br/> 21<br/>   | s \_ E \_ descriptografar \_ falha<br/> 0x80090330<br/>             |
| \_Estouro de \_ registro de alerta TLS1 \_<br/> 22<br/>     | \_mensagem s E \_ inválida \_<br/> 0x80090326<br/>             |
| \_ \_ Falha na descompactação do alerta SSL3 \_<br/> 30<br/>  | s \_ E \_ mensagem \_ alterada<br/> 0x8009030F<br/>             |
| \_Falha de \_ handshake de alerta SSL3 \_<br/> 40<br/>   | \_mensagem s E \_ inválida \_<br/> 0x80090326<br/>             |
| \_ \_ Certificado inadequado do alerta TLS1 \_<br/> 42<br/>     | s \_ E \_ certificado \_ desconhecido<br/> 0x80090327<br/>                |
| Certificado TLS1 de \_ alerta \_ sem suporte \_<br/> 43<br/>    | s \_ E \_ certificado \_ desconhecido<br/> 0x80090327<br/>                |
| Certificado de alerta do TLS1 \_ \_ \_ revogado<br/> 44<br/> | CRIPTOGRAFAdo \_ E \_ revogado<br/> 0x80092010<br/>                    |
| Certificado de alerta do TLS1 \_ \_ \_ expirado<br/> 45<br/> | s \_ E \_ CERT \_ expiraram<br/> 0x80090328<br/>                |
| Certificado de alerta do TLS1 \_ \_ \_ desconhecido<br/> 46<br/> | s \_ E \_ certificado \_ desconhecido<br/> 0x80090327<br/>                |
| \_ \_ Parâmetro ilegal de alerta SSL3 \_<br/>                 | \_mensagem s E \_ inválida \_<br/> 0x80090326<br/>             |
| \_ \_ AC desconhecida de alerta TLS1 \_<br/> 48<br/>          | s \_ E \_ raiz não confiáveis \_<br/> 0x80090325<br/>              |
| Acesso ao alerta do TLS1 \_ \_ \_ negado<br/> 49<br/>       | s \_ E \_ logon \_ negado<br/> 0x8009030C<br/>                |
| \_Erro de \_ decodificação de alerta TLS1 \_<br/> 50<br/>        | \_mensagem s E \_ inválida \_<br/> 0x80090326<br/>             |
| \_Erro de \_ descriptografia de alerta TLS1 \_<br/> 51<br/>       | s \_ E \_ descriptografar \_ falha<br/> 0x80090330<br/>             |
| \_Restrição de \_ exportação de alerta TLS1 \_<br/> 60<br/>  | \_mensagem s E \_ inválida \_<br/> 0x80090326<br/>             |
| \_Versão do \_ protocolo de alerta TLS1 \_<br/> 70<br/>    | s \_ E \_ função sem suporte \_<br/> 0x80090302<br/>        |
| \_Segurança do \_ insuficiente de alertas do TLS1 \_<br/> 71<br/> | incompatibilidade de \_ algoritmo s E \_ \_<br/> 0x80090331<br/>          |
| \_ \_ Erro interno do alerta TLS1 \_<br/> 80<br/>      | s \_ E \_ \_ erro interno<br/> 0x80090304<br/>              |
| Usuário de alerta do TLS1 \_ \_ \_ cancelado<br/> 90<br/>       | E/s não \_ \_ concluído \_ contexto \_ excluído<br/> 0x80090333<br/> |
| Alerta de TLS1 \_ \_ sem \_ renegociação<br/> 100<br/>   | \_mensagem s E \_ inválida \_<br/> 0x80090326<br/>             |
| EXT. de alerta de TLS1 \_ \_ sem suporte \_<br/> 110<br/>    | \_mensagem s E \_ inválida \_<br/> 0x80090326<br/>             |
| Padrão<br/>                                         | \_mensagem s E \_ inválida \_<br/> 0x80090326<br/>             |



 

 

 
