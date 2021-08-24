---
title: Instalando o provedor
description: o procedimento para instalar o provedor WMI de DNS difere com base na versão do Windows em que ele está instalado.
ms.assetid: 5f2bd11a-bc1d-4a43-92d4-26392d2504e7
keywords:
- Sistema de nomes de domínio, provedor WMI, instalando
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1a9b4b976ccb1a600f56042cb75b500577335059966a82dbb1f9e77b04f7a4df
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119693036"
---
# <a name="installing-the-provider"></a>Instalando o provedor

o procedimento para instalar o provedor WMI de DNS difere com base na versão do Windows em que ele está instalado. o procedimento a seguir descreve como instalar e configurar o provedor WMI de DNS no Windows 2000. para obter o provedor WMI de DNS para Windows 2000, baixe o seguinte arquivo:

**AVISO:** Os arquivos do provedor WMI do DNS não são intercambiáveis. Windows servidores dns 2000 exigem arquivos diferentes e um procedimento diferente dos servidores dns do Windows Server 2003. O procedimento para cada um é fornecido.

**para instalar o provedor WMI de DNS no servidor Windows 2000**

1.  obtenha o provedor WMI de DNS para Windows 2000 do Windows o Kit de recursos de servidor do 2000 ou baixe o arquivo, Dnsprov.zip, de: ftp://ftp.microsoft.com/reskit/win2000/
2.  Copie o provedor WMI de DNS (Dnsprov.dll) e os arquivos Dnsschema. MOF para o diretório system32 do webprovider <winntdir> \\ \\ .
3.  Compile o arquivo MOF. Isso personaliza o esquema para corresponder ao servidor.

    **Mofcomp dnsschema. mof**

4.  Registre a DLL no servidor DNS.

    **dnsprov.dllregsvr32**

5.  Os scripts ou programas que usam o provedor WMI de DNS para gerenciar servidores DNS podem ser usados. Os scripts ou programas podem ser executados por meio do servidor DNS ou de um computador cliente.
    > [!Note]  
    > O SDK do WMI não é necessário para executar o provedor WMI de DNS, mas ele contém muitas ferramentas úteis.

     

O provedor WMI de DNS deve ser instalado em qualquer servidor DNS a ser gerenciado; os scripts DNS, no entanto, podem ser executados no servidor DNS ou em um host remoto.

**para instalar o provedor WMI de DNS no Windows Server 2003**

-   para sistemas operacionais Windows Server 2003, o provedor WMI de DNS é automaticamente instalado e registrado, e seu arquivo MOF é compilado quando o serviço do servidor DNS é instalado.

 

 




