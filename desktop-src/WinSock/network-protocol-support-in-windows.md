---
description: O Internet Protocol Suite é o protocolo de rede dominante usado em redes corporativas e pela Internet.
ms.assetid: 8c123e09-b11a-4c92-b41e-49cc01be53d3
title: Suporte ao protocolo de rede Winsock no Windows
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 36da53101dda06426a04e5f910b4548273e8ab47
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104461111"
---
# <a name="winsock-network-protocol-support-in-windows"></a>Suporte ao protocolo de rede Winsock no Windows

O Internet Protocol Suite é o protocolo de rede dominante usado em redes corporativas e pela Internet. O conjunto de protocolos de Internet representa uma grande coleção de protocolos de rede em camadas. O pacote de protocolo de Internet é geralmente conhecido como TCP/IP com base em dois dos protocolos mais importantes incluídos no conjunto: o protocolo IP e o protocolo TCP.

O IPv6 e o IPv4 representam as duas versões disponíveis do protocolo de Internet. O TCP é um dos vários serviços de rede importantes geralmente chamados de protocolos IP que operam em redes IPv6 e IPv4. O protocolo UDP (User Datagram Protocol) e o protocolo ICMP são outros protocolos IP importantes usados em redes IPv6 e IPv4. Há vários outros protocolos IP que podem ser usados em redes IPv6 e IPv4.

O Windows Sockets considera cada conjunto de protocolos de rede como uma família de endereços exclusiva. Portanto, o protocolo IPv6 é considerado a família de endereços **\_ INET6 de AF** e o protocolo IPv4 é considerado a família de endereços **\_ inet** da série AF. Os protocolos IPv6 e IPv4 oferecem suporte ao uso de vários protocolos IP em camadas, como TCP, UDP e ICMP.

O Windows Sockets foi inicialmente projetado para adicionar suporte para IPv4 ao Windows. No entanto, a interface de programação do Windows Sockets foi criada a partir do início com a capacidade de dar suporte a outros conjuntos de protocolo de rede. Com o passar do tempo, as versões do Windows e os soquetes do Windows associados incluíram suporte nativo para outros conjuntos de protocolo de rede (IPX/SPX e AppleTalk, por exemplo). O suporte para outros protocolos de rede também estava disponível para versões do Windows como software de terceiros dos fornecedores.

Antes do crescimento e da popularidade da Internet, vários outros conjuntos de protocolo de rede foram usados em ambientes em rede, especialmente para intranets locais. A escolha de um pacote de protocolo de rede geralmente era baseada no tamanho da rede ou na experiência da equipe de rede de ti. Com a conectividade global de Internet atual vinculando até mesmo as menores redes ao resto do mundo, a experiência de rede no IPv6 e no IPv4 é essencial para os profissionais de rede. Como resultado, outros conjuntos de protocolo de rede importantes anteriormente agora estão em uso muito limitado e se tornaram obviated. O suporte nativo para esses conjuntos de protocolo de rede obviated, geralmente conhecido como protocolos de rede herdados, foi descartado das versões recentes do Microsoft Windows. O suporte para alguns desses protocolos herdados pode estar disponível como software de terceiros de fornecedores (ATM com hardware de rede ATM, por exemplo).

A tabela a seguir identifica o suporte nativo do Windows para conjuntos de protocolo de rede comuns. 

| Protocolo de rede                 | Windows 7                | Windows Server 2008      | Windows Vista            | Windows Server 2003                  | Windows XP                           | Windows 2000                         |
|----------------------------------|--------------------------|--------------------------|--------------------------|--------------------------------------|--------------------------------------|--------------------------------------|
| IPv6<br/>                  | Com suporte<br/>     | Com suporte<br/>     | Com suporte<br/>     | Com suporte<br/>                 | Com suporte<br/>                 | Sem suporte (consulte as observações)<br/> |
| IPv4<br/>                  | Com suporte<br/>     | Com suporte<br/>     | Com suporte<br/>     | Com suporte<br/>                 | Com suporte<br/>                 | Com suporte<br/>                 |
| NetBIOS (consulte as observações) <br/>  | Com suporte<br/>     | Com suporte<br/>     | Com suporte<br/>     | Com suporte<br/>                 | Com suporte<br/>                 | Com suporte<br/>                 |
| IrDA (consulte Observações)<br/>      | Com suporte<br/>     | Com suporte<br/>     | Com suporte<br/>     | Com suporte<br/>                 | Com suporte<br/>                 | Com suporte<br/>                 |
| Bluetooth (consulte Observações)<br/> | Com suporte<br/>     | Com suporte<br/>     | Com suporte<br/>     | Com suporte<br/>                 | Com suporte<br/>                 | Sem suporte<br/>             |
| IPX/SPX<br/>               | Sem suporte<br/> | Sem suporte<br/> | Sem suporte<br/> | Com suporte<br/>                 | Com suporte<br/>                 | Com suporte<br/>                 |
| Numa<br/>             | Sem suporte<br/> | Sem suporte<br/> | Sem suporte<br/> | Com suporte<br/>                 | Com suporte<br/>                 | Com suporte<br/>                 |
| DLC<br/>                   | Sem suporte<br/> | Sem suporte<br/> | Sem suporte<br/> | Sem suporte (consulte as observações)<br/> | Sem suporte (consulte as observações)<br/> | Com suporte<br/>                 |
| ATM<br/>                   | Sem suporte<br/> | Sem suporte<br/> | Sem suporte<br/> | Com suporte (consulte as observações)<br/>     | Com suporte (consulte as observações)<br/>     | Com suporte (consulte as observações)<br/>     |
| NetBEUI<br/>               | Sem suporte<br/> | Sem suporte<br/> | Sem suporte<br/> | Sem suporte<br/>             | Sem suporte<br/>             | Com suporte (consulte as observações)<br/>     |



 

**IPv6 no Windows 2000:** O protocolo IPv6 tem suporte no Windows 2000 com Service Pack 1 (SP1) e posterior com o Microsoft IPv6 Technology Preview para Windows 2000.

**NetBIOS:** O protocolo NetBIOS é normalmente usado pelos serviços de nomenclatura no Windows. O NetBIOS pode usar vários conjuntos de protocolo de rede, incluindo IP (NetBIOS sobre TCP/IP), IPX/SPX e NetBEUI. O Winsock dá suporte a NetBIOS sobre TCP/IP (normalmente chamada de NetBT) somente nas versões de 32 bits do Windows 7, Windows Server 2008 e Windows Vista. O Winsock dá suporte a NetBIOS sobre TCP/IP e NetBIOS usando IPX no Windows Server 2003 e no Windows XP. O Winsock dá suporte a NetBIOS sobre TCP/IP, NetBIOS usando IPX e NetBIOS usando NetBEUI no Windows 2000.

**IrDA:** O protocolo IrDA (Associação de dados de infravermelho) terá suporte se o computador tiver uma porta de infravermelho e driver instalado.

**Bluetooth:** O suporte a Winsock para Bluetooth como um pacote de protocolo de rede inclui os perfis de PAN (rede de área pessoal) Bluetooth e DUN (rede dial up). O suporte a Bluetooth no Windows também inclui o uso do dispositivos de interface humana Bluetooth (HID) e outros perfis para conectar-se a teclados, dispositivos apontadores e outros dispositivos de entrada que não estão relacionados a protocolos de rede.

**DLC no windows 2003 e Windows XP:** O protocolo DLC (controle de vínculo de dados) tem suporte no Windows Server 2003 e no Windows XP quando o driver DLC incluído com o Microsoft Host Integration Server 2006, Host Integration Server 2004 ou Host Integration Server 2000 está instalado.

**ATM no windows 2003, Windows XP e windows 2000:** O protocolo ATM (modo de transferência assíncrona) tem suporte no Windows Server 2003, Windows XP e Windows 2000 quando um adaptador de rede ATM é instalado. O protocolo para o IP clássico sobre ATM (às vezes abreviado como CLIP/ATM) é definido em [RFC 2225](https://tools.ietf.org/html/rfc2225) e documentos relacionados publicados pela IETF. O Windows Server 2003, o Windows XP e o Windows 2000 fornecem uma implementação completa desse padrão.

**NetBEUI no Windows 2000:** O protocolo NetBEUI não tem suporte direto do Windows Sockets. Mas o protocolo NetBIOS que pode usar vários protocolos de rede dá suporte ao uso do protocolo NetBEUI no Windows 2000.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Referência técnica do ATM](/previous-versions/windows/it-pro/windows-server-2003/cc759707(v=ws.10))
</dt> <dt>

[Bluetooth](../bluetooth/bluetooth-start-page.md)
</dt> <dt>

[Versão prévia da tecnologia IPv6 para Windows 2000](https://www.microsoft.com/downloads/details.aspx?FamilyID=27b1e6a6-bbdd-43c9-af57-dae19795a088)
</dt> <dt>

[IrDA](/previous-versions/windows/desktop/irda/irda-start-page)
</dt> <dt>

[Suporte a NDIS 5,0 e ATM no Windows](/windows-hardware/drivers/network/ndis-version-guide)
</dt> </dl>

 

 
