---
description: A Microsoft implementou uma matriz de extensões para o formato de arquivo de configuração automática do Navigator a fim de adicionar suporte a IPv6 nas funções auxiliares de WPAD do WinINet e do WinHTTP.
ms.assetid: 40116a01-b18f-432a-8542-b56b3f55c692
title: Formato de arquivo de configuração automática de extensões IPv6 para navegador
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6a6db6d687cfde0c3289026e8fa36c77c3ff5372727d1604652160b0683169b8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119644005"
---
# <a name="ipv6-extensions-to-navigator-auto-config-file-format"></a>Formato de arquivo de configuração automática de extensões IPv6 para navegador

A Microsoft implementou uma matriz de extensões para o formato de arquivo de configuração automática do Navigator a fim de adicionar suporte a IPv6 nas funções auxiliares de WPAD do WinINet e do WinHTTP.

A explosão da Internet no final de 1990 causou um escassez inesperado de endereços IPv4, com o pool esgotado diariamente. O IPv6 fornece uma solução para esse problema e, embora não esteja amplamente implantado, seu uso definitivamente se tornará mais predominante no futuro. [WPAD](https://www.ietf.org/proceedings/45/I-D/draft-ietf-wrec-wpad-00.txt) é um protocolo que permite que os clientes Web detectem automaticamente o que a configuração correta de proxy deve ser para o tráfego de saída. Isso é muito útil para implantações corporativas porque permite que os administradores de ti configurem scripts complexos que podem rotear o tráfego para todos os clientes para proxies específicos com base no servidor de destino ao qual os clientes estão tentando se conectar. O WinINet e o WinHTTP dão suporte a funções auxiliares WPAD, conforme definido pela [especificação de formato de Arquivo PAC (configuração automática de proxy do navegador)](https://web.archive.org/web/20060424005037/wp.netscape.com/eng/mozilla/2.0/relnotes/demo/proxy-live.html), que se tornou um padrão de fato. Infelizmente, essa especificação foi escrita em 1996 e não define o que os comportamentos de função devem ser quando um script WPAD é implantado em uma rede compatível com IPv6.

como o IPv6 é a onda do futuro, todos os componentes de Windows agora dão suporte a pilha dupla (IPv4 e ipv6) e somente a redes ipv6. Para dar suporte a IPv6 sem afetar a implantação existente, a Microsoft adicionou 6 novas funções de classe auxiliar como uma extensão para a especificação de formato de Arquivo PAC (auto-config) do navegador e também adicionou uma nova função compatível com IPv6 chamada **FindProxyForURLEx** que os administradores podem implementar no script WPAD.

<dl> <dt>

[Definições da API auxiliar de proxy com reconhecimento de IPv6](ipv6-aware-proxy-helper-api-definitions.md)
</dt> <dd></dd> <dt>

[Diferenças entre IPv6-Aware funções auxiliares WPAD e funções auxiliares WPAD herdadas](differences-between-ipv6-aware-wpad-helper-functions-and-legacy-wpad-helper-functions.md)
</dt> <dd></dd> </dl>

> [!Note]  
> essa funcionalidade requer Windows Internet Explorer 7 ou superior.

 

 

 



