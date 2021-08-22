---
description: O método estático da classe WMI SetIGMPLevel é usado para definir a extensão até a qual o sistema dá suporte à multicasting de IP e participa do Protocolo de Gerenciamento de Grupo da Internet.
ms.assetid: 38877576-aa23-4841-b3ae-1a02bfdd70d8
ms.tgt_platform: multiple
title: Método SetIGMPLevel da classe Win32_NetworkAdapterConfiguration classe
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_NetworkAdapterConfiguration.SetIGMPLevel
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 20ca9874447f4d606f7559dc60322f206c4726feb5cbe070b188bb04173427ea
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119439996"
---
# <a name="setigmplevel-method-of-the-win32_networkadapterconfiguration-class"></a>Método SetIGMPLevel da classe \_ NetworkAdapterConfiguration do Win32

O método estático da classe [WMI](/windows/desktop/WmiSdk/retrieving-a-class) **SetIGMPLevel** é usado para definir a extensão até a qual o sistema dá suporte à multicasting de IP e participa do Protocolo de Gerenciamento de Grupo da Internet.

Este tópico usa sintaxe Managed Object Format (MOF). Para obter mais informações sobre como usar esse método, consulte [Chamando um método](/windows/desktop/WmiSdk/calling-a-method).

## <a name="syntax"></a>Sintaxe


```mof
uint32 SetIGMPLevel(
  [in] uint8 IGMPLevel
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*IGMPLevel* \[ Em\]
</dt> <dd>

Tipo de dados: **Inteiro**

Define o nível no qual o sistema dá suporte a multicast de IP e participa do Protocolo de Gerenciamento de Grupo da Internet. No nível 0, o sistema não oferece suporte a multicast. No nível 1, o sistema só pode enviar pacotes de multicast IP. No nível 2, o sistema pode enviar pacotes de multicast IP e participar totalmente do IGMP para receber pacotes multicast.

<dt>

<span id="No_Multicast"></span><span id="no_multicast"></span><span id="NO_MULTICAST"></span>

**Sem Multicast** (0)


</dt> <dd></dd> <dt>

<span id="IP_Multicast"></span><span id="ip_multicast"></span><span id="IP_MULTICAST"></span>

**Multicast de IP** (1)


</dt> <dd></dd> <dt>

<span id="IP___IGMP_multicast"></span><span id="ip___igmp_multicast"></span><span id="IP___IGMP_MULTICAST"></span>

**Multicast IGMP & IP** (2)


</dt> <dd></dd> </dl> </dd> </dl>

## <a name="return-value"></a>Valor retornado

Retorna um valor de 0 (zero) para uma conclusão bem-sucedida quando nenhuma reinicialização é necessária, 1 (um) para uma conclusão bem-sucedida quando uma reinicialização é necessária e um número diferente se houver um erro. Para obter mais informações sobre códigos de erro, consulte [**Constantes de erro WMI**](/windows/desktop/WmiSdk/wmi-error-constants) ou [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum). Para valores **gerais de HRESULT,** consulte [Códigos de erro do sistema.](/windows/desktop/Debug/system-error-codes)

<dl> <dt>

**Conclusão bem-sucedida, nenhuma reinicialização necessária**
</dt> <dd>

0

Conclusão bem-sucedida, sem necessidade de reinicialização.

</dd> <dt>

**Conclusão bem-sucedida, reinicialização necessária**
</dt> <dd>

1

Conclusão bem-sucedida, reinicialização necessária.

</dd> <dt>

**Método sem suporte nesta plataforma**
</dt> <dd>

64

Não há suporte para o método nesta plataforma.

</dd> <dt>

**Falha desconhecida**
</dt> <dd>

65

Falha desconhecida.

</dd> <dt>

**Máscara de sub-rede inválida**
</dt> <dd>

66

Máscara de sub-rede inválida.

</dd> <dt>

**Ocorreu um erro ao processar uma Instância que foi retornada**
</dt> <dd>

67

Ocorreu um erro ao processar uma instância que foi retornada.

</dd> <dt>

**Parâmetro de entrada inválido**
</dt> <dd>

68

Parâmetro de entrada inválido.

</dd> <dt>

**Mais de 5 gateways especificados**
</dt> <dd>

69

Mais de cinco gateways especificados.

</dd> <dt>

**Endereço IP inválido**
</dt> <dd>

70

Endereço IP inválido.

</dd> <dt>

**Endereço IP do gateway inválido**
</dt> <dd>

71

Endereço IP do gateway inválido.

</dd> <dt>

**Ocorreu um erro ao acessar o Registro para as informações solicitadas**
</dt> <dd>

72

Ocorreu um erro ao acessar o Registro para as informações solicitadas.

</dd> <dt>

**Nome de domínio inválido**
</dt> <dd>

73

Nome de domínio inválido.

</dd> <dt>

**Nome de host inválido**
</dt> <dd>

74

Nome de host inválido.

</dd> <dt>

**Nenhum servidor WINS primário/secundário definido**
</dt> <dd>

75

Nenhum servidor WINS primário ou secundário definido.

</dd> <dt>

**Arquivo inválido**
</dt> <dd>

76

Arquivo inválido.

</dd> <dt>

**Caminho do sistema inválido**
</dt> <dd>

77

Caminho do sistema inválido.

</dd> <dt>

**Falha na cópia do arquivo**
</dt> <dd>

78

Falha na cópia do arquivo.

</dd> <dt>

**Parâmetro de segurança inválido**
</dt> <dd>

79

Parâmetro de segurança inválido.

</dd> <dt>

**Não é possível configurar o serviço TCP/IP**
</dt> <dd>

80

Não é possível configurar o serviço TCP/IP.

</dd> <dt>

**Não é possível configurar o serviço DHCP**
</dt> <dd>

81

Não é possível configurar o serviço DHCP.

</dd> <dt>

**Não é possível renovar a concessão de DHCP**
</dt> <dd>

82

Não é possível renovar a concessão de DHCP.

</dd> <dt>

**Não é possível liberar a concessão de DHCP**
</dt> <dd>

83

Não é possível liberar a concessão de DHCP.

</dd> <dt>

**IP não habilitado no adaptador**
</dt> <dd>

84

IP não habilitado no adaptador.

</dd> <dt>

**IPX não habilitado no adaptador**
</dt> <dd>

85

IPX não habilitado no adaptador.

</dd> <dt>

**Erro de limites de número de quadro/rede**
</dt> <dd>

86

Erro de limites de quadro ou número de rede.

</dd> <dt>

**Tipo de quadro inválido**
</dt> <dd>

87

Tipo de quadro inválido.

</dd> <dt>

**Número de rede inválido**
</dt> <dd>

88

Número de rede inválido.

</dd> <dt>

**Número de rede duplicado**
</dt> <dd>

89

Número de rede duplicado.

</dd> <dt>

**Parâmetro fora dos limites**
</dt> <dd>

90

Parâmetro fora dos limites.

</dd> <dt>

**Acesso negado**
</dt> <dd>

91

Acesso negado

</dd> <dt>

**Memória insuficiente**
</dt> <dd>

92

Sem memória.

</dd> <dt>

**Já existe**
</dt> <dd>

93

Já existe.

</dd> <dt>

**Caminho, arquivo ou objeto não encontrado**
</dt> <dd>

94

Caminho, arquivo ou objeto não encontrado.

</dd> <dt>

**Não é possível notificar o serviço**
</dt> <dd>

95

Não é possível notificar o serviço.

</dd> <dt>

**Não é possível notificar o serviço DNS**
</dt> <dd>

96

Não é possível notificar o serviço DNS.

</dd> <dt>

**Interface não configurável**
</dt> <dd>

97

Interface não configurável.

</dd> <dt>

**Nem todas as concessões DHCP puderam ser liberadas/renovadas**
</dt> <dd>

98

Nem todas as concessões DHCP podem ser liberadas ou renovadas.

</dd> <dt>

**DHCP não habilitado no adaptador**
</dt> <dd>

100

DHCP não habilitado no adaptador.

</dd> <dt>

**Outras**
</dt> <dd>

101 4294967295

</dd> </dl>

## <a name="examples"></a>Exemplos

A amostra [Modificar o nível IGMP para todos os adaptadores de rede do](https://Gallery.TechNet.Microsoft.Com/b92f894c-5cf8-4484-b5f0-d54761bacd5c) VBScript desabilita o multicast IGMP em um computador.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Vista<br/>                                                                |
| Servidor mínimo com suporte<br/> | Windows Server 2008<br/>                                                          |
| Namespace<br/>                | Raiz \\ cimv2<br/>                                                                  |
| MOF<br/>                      | <dl> <dt>CIMWin32. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>CIMWin32.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Classes de hardware do sistema de computador](computer-system-hardware-classes.md)
</dt> <dt>

[**\_NetworkAdapterConfiguration Win32**](win32-networkadapterconfiguration.md)
</dt> <dt>

[Tarefas do WMI: rede](/windows/desktop/WmiSdk/wmi-tasks--networking)
</dt> <dt>

[Tarefas do WMI: contas e domínios](/windows/desktop/WmiSdk/wmi-tasks--accounts-and-domains)
</dt> <dt>

[Suporte a IPv6 e IPv4 no WMI](/windows/desktop/WmiSdk/ipv6-and-ipv4-support-in-wmi)
</dt> </dl>

 

