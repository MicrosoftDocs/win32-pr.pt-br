---
description: Define o número de rede virtual de intercâmbio de pacotes entre redes (IPX) no sistema de computador de destino.
ms.assetid: 52064250-b94f-4dc0-bf1a-8601cd135a90
ms.tgt_platform: multiple
title: Método SetIPXVirtualNetworkNumber da classe Win32_NetworkAdapterConfiguration
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_NetworkAdapterConfiguration.SetIPXVirtualNetworkNumber
api_type:
- COM
api_location:
- cimwin32.dll
ms.openlocfilehash: ed6e6802a17ef6ec4393d2ae0c5ec43f0e21d247
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105762760"
---
# <a name="setipxvirtualnetworknumber-method-of-the-win32_networkadapterconfiguration-class"></a>Método SetIPXVirtualNetworkNumber da classe Win32 \_ NetworkAdapterConfiguration

Define o número de rede virtual de intercâmbio de pacotes entre redes (IPX) no sistema de computador de destino. O Windows 2000 e o Windows NT 3,51 ou superior usam um número de rede interno para roteamento interno. O número de rede interno também é conhecido como um número de rede virtual. Ele identifica exclusivamente o sistema de computador na rede. O método retorna um valor inteiro que pode ser interpretado da seguinte maneira:

## <a name="syntax"></a>Sintaxe


```mof
uint32 SetIPXVirtualNetworkNumber(
  [in] string IPXVirtualNetNumber
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*IPXVirtualNetNumber* \[ no\]
</dt> <dd>

O número da rede virtual para este sistema.

</dd> </dl>

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

 

 




