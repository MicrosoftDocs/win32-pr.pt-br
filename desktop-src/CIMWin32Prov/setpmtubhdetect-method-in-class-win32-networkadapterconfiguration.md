---
description: O método estático da classe WMI SetPMTUBHDetect é usado para habilitar a detecção de roteadores de Black Hole ao fazer a Descoberta de MTU de Caminho.
ms.assetid: a1e45ed9-85a9-4fdd-890a-d578c3f94b72
ms.tgt_platform: multiple
title: Método SetPMTUBHDetect da classe Win32_NetworkAdapterConfiguration
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_NetworkAdapterConfiguration.SetPMTUBHDetect
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: c9b97e7c55c03dc2fe0e899f9878310eebbf395e3ff15631cea6db8c98546e3a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119439826"
---
# <a name="setpmtubhdetect-method-of-the-win32_networkadapterconfiguration-class"></a>Método SetPMTUBHDetect da classe \_ NetworkAdapterConfiguration do Win32

O método estático da classe [WMI](/windows/desktop/WmiSdk/retrieving-a-class) **SetPMTUBHDetect** é usado para habilitar a detecção de roteadores de Black Hole ao fazer a Descoberta de MTU de Caminho.

Este tópico usa sintaxe Managed Object Format (MOF). Para obter mais informações sobre como usar esse método, consulte [Chamando um método](/windows/desktop/WmiSdk/calling-a-method).

## <a name="syntax"></a>Sintaxe


```mof
uint32 SetPMTUBHDetect(
  [in] boolean PMTUBHDetectEnabled
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*PMTUBHDetectEnabled* \[ Em\]
</dt> <dd>

Se **for true,** o TCP tentará descobrir o Black Hole e rotear pacotes em caminhos de rede diferentes.

</dd> </dl>

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

**Nem todas as concessões DHCP podem ser liberadas/renovadas**
</dt> <dd>

98

Nem todas as concessões DHCP podem ser liberadas ou renovadas.

</dd> <dt>

**DHCP não habilitado no adaptador**
</dt> <dd>

100

O DHCP não está habilitado no adaptador.

</dd> <dt>

**Outras**
</dt> <dd>

101 4294967295

</dd> </dl>

## <a name="remarks"></a>Comentários

Um roteador de Black Hole não retorna as mensagens de destino icmp (protocolo ICMP) inacessível quando precisa fragmentar um datagrama IP com o conjunto de bits Não Fragmentar. O TCP depende do recebimento dessas mensagens para executar a Descoberta de MTU de Caminho.

Com esse recurso habilitado, o TCP tentará enviar segmentos sem o conjunto de bits Não Fragmentar se várias retransmissões de um segmento não são conhecidas. Se o segmento for confirmado como resultado, o MSS (tamanho máximo do segmento) será reduzido e o bit Não Fragmentar será definido em pacotes futuros na conexão. A habilitação da detecção de orifícios pretos aumenta o número máximo de retransmissões executadas para um determinado segmento.

## <a name="examples"></a>Exemplos

A [opção Modificar Detecção de PMTUBH](https://Gallery.TechNet.Microsoft.Com/a576d97b-38fe-437e-a632-d2f7e122301c) em Todos os Adaptadores de Rede permite a descoberta automática de roteadores de orifício preto ao determinar a unidade de transmissão máxima em uma rede.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Vista<br/>                                                                |
| Servidor mínimo com suporte<br/> | Windows Server 2008<br/>                                                          |
| Namespace<br/>                | RAIZ \\ CIMV2<br/>                                                                  |
| MOF<br/>                      | <dl> <dt>CIMWin32.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>CIMWin32.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Classes de hardware do sistema de computador](computer-system-hardware-classes.md)
</dt> <dt>

[**Win32 \_ NetworkAdapterConfiguration**](win32-networkadapterconfiguration.md)
</dt> <dt>

[Tarefas WMI: Rede](/windows/desktop/WmiSdk/wmi-tasks--networking)
</dt> <dt>

[Tarefas WMI: contas e domínios](/windows/desktop/WmiSdk/wmi-tasks--accounts-and-domains)
</dt> <dt>

[Suporte a IPv6 e IPv4 no WMI](/windows/desktop/WmiSdk/ipv6-and-ipv4-support-in-wmi)
</dt> </dl>

 

