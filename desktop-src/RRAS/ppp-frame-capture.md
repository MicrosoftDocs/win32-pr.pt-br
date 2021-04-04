---
title: Escrevendo um driver para capturar quadros PPP
description: Este documento explica como desenvolver um driver que pode capturar quadros PPP no Windows Vista antes que eles sejam compactados/criptografados no caminho de envio ou depois de serem descompactados/descriptografados no caminho de recebimento.
ms.assetid: 1b3fe1b8-2b11-4aed-98e1-464b8c0821ec
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d592596674cd64af5122303afefcfc81026dad27
ms.sourcegitcommit: 3e70ae762629e244028b437420ed50b5850db4e3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/20/2020
ms.locfileid: "104007163"
---
# <a name="writing-a-driver-to-capture-ppp-frames"></a>Escrevendo um driver para capturar quadros PPP

Quando os quadros de protocolo PPP (PPP) são enviados por meio de um túnel PPTP com criptografia ativada, ou por meio de um túnel L2TP (protocolo de encapsulamento de camada 2) que usa IPSec para criptografia, o utilitário de captura de quadro PPP típico só pode capturar quadros PPP que tenham um campo de identidade de protocolo criptografado. Este documento explica como desenvolver um driver que pode capturar quadros PPP no Windows Vista antes que eles sejam compactados/criptografados no caminho de envio ou depois de serem descompactados/descriptografados no caminho de recebimento.

1.  Escreva um driver de protocolo NDIS. Para obter detalhes, consulte [drivers de protocolo ndis 6,0](https://msdn.microsoft.com/library/ms795570.aspx) ou [drivers de protocolo ndis (NDIS 5,1)](https://msdn.microsoft.com/library/ms801145.aspx).
2.  Instale o driver com uma identidade de hardware de "MS \_ Netmon". Para obter instruções detalhadas sobre como instalar o driver com uma identidade de hardware específica, consulte a [seção modelos inf](https://msdn.microsoft.com/library/ms794357.aspx).
    > [!Note]  
    > Cada computador com Windows Vista permite a instalação de apenas uma entidade de driver que tenha a \_ identidade de hardware "MS Netmon". Para instalar outro driver com essa identidade, o primeiro driver deve ser desinstalado. Um driver que é instalado sem usar a identidade de \_ hardware "MS Netmon" não pode executar a associação necessária para capturar quadros PPP.

     

3.  O driver de protocolo deve especificar "ndiswanbh" como a interface de associação para capturar quadros PPP. Para obter instruções detalhadas, consulte [especificando interfaces de associação](https://msdn.microsoft.com/library/aa937923.aspx).
4.  A implementação de [ProtocolBindAdapter](https://msdn.microsoft.com/library/ms797311.aspx) no driver deve dar suporte a "NdisMediumWan" como parte da matriz média, para que ele possa abrir a borda de miniporta ndiswanbh usando a função [NdisOpenAdapter](https://msdn.microsoft.com/library/ms804862.aspx) .
5.  Se a função [ProtocolOpenAdapterComplete](https://msdn.microsoft.com/library/ms797287.aspx) for chamada com status êxito de status de NDIS \_ \_ , o driver de protocolo deverá definir o OID [Gen do \_ \_ \_ \_ filtro de pacotes atual](https://msdn.microsoft.com/library/bb314089.aspx) com os sinalizadores tipo de pacote de [NDIS \_ \_ \_ promíscuo](https://msdn.microsoft.com/library/bb314089.aspx) e [tipo de pacote de NDIS \_ \_ \_ todos os \_ locais](https://msdn.microsoft.com/library/bb314089.aspx) nessa associação. Quando isso for feito, o driver de protocolo receberá os quadros PPP descriptografados da camada de enquadramento PPP em sua função [ProtocolReceive](https://msdn.microsoft.com/library/ms797274.aspx) .

> [!Note]  
> Essas informações se aplicam somente a drivers em um computador com Windows Vista.

 

 

 




