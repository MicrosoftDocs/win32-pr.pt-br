---
title: Instalando o provedor
description: O procedimento para instalar o provedor WMI de DNS difere com base na versão do Windows em que está instalado.
ms.assetid: 5f2bd11a-bc1d-4a43-92d4-26392d2504e7
keywords:
- Sistema de nomes de domínio, provedor WMI, instalando
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3b1c9dbdaf6d3ad55247d0b978c0a422361a2f04
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103635284"
---
# <a name="installing-the-provider"></a>Instalando o provedor

O procedimento para instalar o provedor WMI de DNS difere com base na versão do Windows em que está instalado. O procedimento a seguir descreve como instalar e configurar o provedor WMI de DNS no Windows 2000. Para obter o provedor WMI de DNS para o Windows 2000, baixe o seguinte arquivo:

**AVISO:** Os arquivos do provedor WMI do DNS não são intercambiáveis. Os servidores DNS do Windows 2000 exigem arquivos diferentes e um procedimento diferente dos servidores DNS do Windows Server 2003. O procedimento para cada um é fornecido.

**Para instalar o provedor WMI de DNS no Windows 2000 Server**

1.  Obtenha o provedor WMI do DNS para Windows 2000 do Windows 2000 Server Resource Kit ou baixe o arquivo, Dnsprov.zip, de: ftp://ftp.microsoft.com/reskit/win2000/
2.  Copie o provedor WMI de DNS (Dnsprov.dll) e os arquivos Dnsschema. MOF para o diretório system32 do webprovider <winntdir> \\ \\ .
3.  Compile o arquivo MOF. Isso personaliza o esquema para corresponder ao servidor.

    **Mofcomp dnsschema. mof**

4.  Registre a DLL no servidor DNS.

    **dnsprov.dllregsvr32**

5.  Os scripts ou programas que usam o provedor WMI de DNS para gerenciar servidores DNS podem ser usados. Os scripts ou programas podem ser executados por meio do servidor DNS ou de um computador cliente.
    > [!Note]  
    > O SDK do WMI não é necessário para executar o provedor WMI de DNS, mas ele contém muitas ferramentas úteis.

     

O provedor WMI de DNS deve ser instalado em qualquer servidor DNS a ser gerenciado; os scripts DNS, no entanto, podem ser executados no servidor DNS ou em um host remoto.

**Para instalar o provedor WMI de DNS no Windows Server 2003**

-   Para sistemas operacionais Windows Server 2003, o provedor WMI de DNS é automaticamente instalado e registrado, e seu arquivo MOF é compilado quando o serviço do servidor DNS é instalado.

 

 




