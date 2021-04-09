---
description: Define os pares de número/quadro da rede IPX (troca de pacotes entre redes) para esse adaptador de rede.
ms.assetid: 8190564f-7d9f-4b05-9949-2e732ce36dba
ms.tgt_platform: multiple
title: Método SetIPXFrameTypeNetworkPairs da classe Win32_NetworkAdapterConfiguration
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_NetworkAdapterConfiguration.SetIPXFrameTypeNetworkPairs
api_type:
- COM
api_location:
- cimwin32.dll
ms.openlocfilehash: e4d53ec7b5600a767505e517a02fbf87b5a43d13
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104089532"
---
# <a name="setipxframetypenetworkpairs-method-of-the-win32_networkadapterconfiguration-class"></a>Método SetIPXFrameTypeNetworkPairs da classe Win32 \_ NetworkAdapterConfiguration

Define os pares de número/quadro da rede IPX (troca de pacotes entre redes) para esse adaptador de rede.

O Windows 2000 e o Windows NT 3,51 e superior usam um número de rede IPX para fins de roteamento. Ele é atribuído a cada combinação de tipo de quadro/adaptador de rede configurada no sistema de computador. Esse número às vezes é chamado de "número de rede externa". Ele deve ser exclusivo para cada segmento de rede. Se o tipo de quadro for definido como automático, o número de rede deverá ser zero.

## <a name="syntax"></a>Sintaxe


```mof
uint32 SetIPXFrameTypeNetworkPairs(
  [in] string IPXNetworkNumber[],
  [in] uint32 IPXFrameType[]
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*IPXNetworkNumber* \[ no\]
</dt> <dd>

Uma matriz de caracteres que identifica exclusivamente um adaptador no sistema de computador. O transporte compatível com IPX/SPX do link do NetWare (NWLink) no Windows 2000 e no Windows NT 3,51 ou superior usa dois tipos diferentes de números de rede. Esse número às vezes é chamado de número de rede externa. Ele deve ser exclusivo para cada segmento de rede. Os valores nessa lista de cadeias de caracteres devem ter um valor correspondente no parâmetro IPXFrameType identificando o tipo de quadro de pacote usado para essa rede.

</dd> <dt>

*IPXFrameType* \[ no\]
</dt> <dd>

Uma matriz de inteiros de identificadores de tipo de quadro. Os valores nessa matriz correspondem aos elementos no parâmetro *IPXNetworkNumber* .

<dt>

<span id="Ethernet_II"></span><span id="ethernet_ii"></span><span id="ETHERNET_II"></span>

**Ethernet II** (0)


</dt> <dd></dd> <dt>

<span id="Ethernet_802.3"></span><span id="ethernet_802.3"></span><span id="ETHERNET_802.3"></span>

**Ethernet 802,3** (1)


</dt> <dd></dd> <dt>

<span id="Ethernet_802.2"></span><span id="ethernet_802.2"></span><span id="ETHERNET_802.2"></span>

**Ethernet 802,2** (2)


</dt> <dd></dd> <dt>

<span id="Ethernet_SNAP"></span><span id="ethernet_snap"></span><span id="ETHERNET_SNAP"></span>

**Ajuste de Ethernet** (3)


</dt> <dd></dd> <dt>

<span id="AUTO"></span><span id="auto"></span>

**Automático** (255)


</dt> <dd></dd> </dl> </dd> </dl>

## <a name="return-value"></a>Retornar valor

<dl> <dt>

**Conclusão bem-sucedida, nenhuma reinicialização necessária** (0)
</dt> <dt>

**Conclusão bem-sucedida, reinicialização necessária** (1)
</dt> <dt>

**Método sem suporte nesta plataforma** (64)
</dt> <dt>

**Falha desconhecida** (65)
</dt> <dt>

**Máscara de sub-rede inválida** (66)
</dt> <dt>

**Ocorreu um erro ao processar uma instância que foi retornada** (67)
</dt> <dt>

**Parâmetro de entrada inválido** (68)
</dt> <dt>

**Mais de 5 gateways especificados** (69)
</dt> <dt>

**Endereço IP inválido** (70)
</dt> <dt>

**Endereço IP de gateway inválido** (71)
</dt> <dt>

**Ocorreu um erro ao acessar o registro para as informações solicitadas** (72)
</dt> <dt>

**Nome de domínio inválido** (73)
</dt> <dt>

**Nome de host inválido** (74)
</dt> <dt>

**Nenhum servidor WINS primário/secundário definido** (75)
</dt> <dt>

**Arquivo inválido** (76)
</dt> <dt>

**Caminho de sistema inválido** (77)
</dt> <dt>

**Falha na cópia do arquivo** (78)
</dt> <dt>

**Parâmetro de segurança inválido** (79)
</dt> <dt>

**Não é possível configurar o serviço TCP/IP** (80)
</dt> <dt>

**Não é possível configurar o serviço DHCP** (81)
</dt> <dt>

**Não é possível renovar a concessão DHCP** (82)
</dt> <dt>

**Não é possível liberar a concessão DHCP** (83)
</dt> <dt>

**IP não habilitado no adaptador** (84)
</dt> <dt>

**IPX não habilitado no adaptador** (85)
</dt> <dt>

**Erro de limites de número de quadro/rede** (86)
</dt> <dt>

**Tipo de quadro inválido** (87)
</dt> <dt>

**Número de rede inválido** (88)
</dt> <dt>

**Número de rede duplicado** (89)
</dt> <dt>

**Parâmetro fora dos limites** (90)
</dt> <dt>

**Acesso negado** (91)
</dt> <dt>

**Memória insuficiente** (92)
</dt> <dt>

**Já existe** (93)
</dt> <dt>

**Caminho, arquivo ou objeto não encontrado** (94)
</dt> <dt>

**Não é possível notificar o serviço** (95)
</dt> <dt>

**Não é possível notificar o serviço DNS** (96)
</dt> <dt>

**Interface não configurável** (97)
</dt> <dt>

**Nem todas as concessões DHCP puderam ser liberadas/renovadas** (98)
</dt> <dt>

**DHCP não habilitado no adaptador** (100)
</dt> <dt>

**Outro** (101 – 4294967295)
</dt> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Vista<br/>                                                                |
| Servidor mínimo com suporte<br/> | Windows Server 2008<br/>                                                          |
| Namespace<br/>                | Raiz \\ cimv2<br/>                                                                  |
| MOF<br/>                      | <dl> <dt>CimWin32. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Cimwin32.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**\_NetworkAdapterConfiguration Win32**](win32-networkadapterconfiguration.md)
</dt> </dl>

 

 




