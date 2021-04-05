---
description: Os SetGateways &\# 32; O método de classe WMI especifica uma lista de gateways para rotear pacotes para uma sub-rede que é diferente da sub-rede à qual o adaptador de rede está conectado.
ms.assetid: 240f7aff-7a07-4e0d-af30-7bcabb68c736
ms.tgt_platform: multiple
title: Método SetGateways da classe Win32_NetworkAdapterConfiguration
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_NetworkAdapterConfiguration.SetGateways
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 215bfa736a0f9d67ae587ac1f0e1b4aa394b85d9
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103826488"
---
# <a name="setgateways-method-of-the-win32_networkadapterconfiguration-class"></a>Método SetGateways da classe Win32 \_ NetworkAdapterConfiguration

O método de [classe WMI](/windows/desktop/WmiSdk/retrieving-a-class) **SetGateways** especifica uma lista de gateways para rotear pacotes para uma sub-rede que é diferente da sub-rede à qual o adaptador de rede está conectado.

Este tópico usa a sintaxe formato MOF (MOF). Para obter mais informações sobre como usar esse método, consulte [chamando um método](/windows/desktop/WmiSdk/calling-a-method).

## <a name="syntax"></a>Sintaxe


```mof
uint32 SetGateways(
  [in]           string DefaultIPGateway[],
  [in, optional] uint16 GatewayCostMetric[]
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*DefaultIPGateway* \[ no\]
</dt> <dd>

Lista de endereços IP para gateways em que os pacotes de rede são roteados.

</dd> <dt>

*GatewayCostMetric* \[ em, opcional\]
</dt> <dd>

Atribui um valor que varia de 1 a 9999, que é usado para calcular as rotas mais rápidas e confiáveis. Os valores desse parâmetro correspondem aos valores no parâmetro *DefaultIPGateway* . O valor padrão para um gateway é 1.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Retorna um valor de 0 (zero) para uma conclusão bem-sucedida quando uma reinicialização não é necessária, 1 (uma) para uma conclusão bem-sucedida quando uma reinicialização é necessária e qualquer outro valor se houver um erro. Para obter mais informações sobre códigos de erro, consulte [**WMI Error Constants**](/windows/desktop/WmiSdk/wmi-error-constants) or [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum). Para obter valores gerais de **HRESULT** , consulte [códigos de erro do sistema](/windows/desktop/Debug/system-error-codes).

<dl> <dt>

**Conclusão bem-sucedida, nenhuma reinicialização necessária**
</dt> <dd>

0

</dd> <dt>

**Conclusão bem-sucedida, reinicialização necessária**
</dt> <dd>

1

</dd> <dt>

**Método sem suporte nesta plataforma**
</dt> <dd>

64

Não há suporte para o método quando a NIC está no modo DHCP.

</dd> <dt>

**Falha desconhecida**
</dt> <dd>

65

</dd> <dt>

**Máscara de sub-rede inválida**
</dt> <dd>

66

</dd> <dt>

**Ocorreu um erro ao processar uma instância que foi retornada**
</dt> <dd>

67

</dd> <dt>

**Parâmetro de entrada inválido**
</dt> <dd>

68

</dd> <dt>

**Mais de 5 gateways especificados**
</dt> <dd>

69

</dd> <dt>

**Endereço IP inválido**
</dt> <dd>

70

</dd> <dt>

**Endereço IP de gateway inválido**
</dt> <dd>

71

</dd> <dt>

**Ocorreu um erro ao acessar o registro para as informações solicitadas**
</dt> <dd>

72

</dd> <dt>

**Nome de domínio inválido**
</dt> <dd>

73

</dd> <dt>

**Nome de host inválido**
</dt> <dd>

74

</dd> <dt>

**Nenhum servidor WINS primário/secundário definido**
</dt> <dd>

75

</dd> <dt>

**Arquivo inválido**
</dt> <dd>

76

</dd> <dt>

**Caminho de sistema inválido**
</dt> <dd>

77

</dd> <dt>

**Falha na cópia do arquivo**
</dt> <dd>

78

</dd> <dt>

**Parâmetro de segurança inválido**
</dt> <dd>

79

</dd> <dt>

**Não é possível configurar o serviço TCP/IP**
</dt> <dd>

80

</dd> <dt>

**Não é possível configurar o serviço DHCP**
</dt> <dd>

81

</dd> <dt>

**Não é possível renovar a concessão DHCP**
</dt> <dd>

82

</dd> <dt>

**Não é possível liberar a concessão DHCP**
</dt> <dd>

83

</dd> <dt>

**IP não habilitado no adaptador**
</dt> <dd>

84

</dd> <dt>

**IPX não habilitado no adaptador**
</dt> <dd>

85

</dd> <dt>

**Erro de limites de número de quadro/rede**
</dt> <dd>

86

</dd> <dt>

**Tipo de quadro inválido**
</dt> <dd>

87

</dd> <dt>

**Número de rede inválido**
</dt> <dd>

88

</dd> <dt>

**Número de rede duplicado**
</dt> <dd>

89

</dd> <dt>

**Parâmetro fora dos limites**
</dt> <dd>

90

</dd> <dt>

**Acesso negado**
</dt> <dd>

91

</dd> <dt>

**Memória insuficiente**
</dt> <dd>

92

</dd> <dt>

**Já existe**
</dt> <dd>

93

</dd> <dt>

**Caminho, arquivo ou objeto não encontrado**
</dt> <dd>

94

</dd> <dt>

**Não é possível notificar o serviço**
</dt> <dd>

95

</dd> <dt>

**Não é possível notificar o serviço DNS**
</dt> <dd>

96

</dd> <dt>

**Interface não configurável**
</dt> <dd>

97

</dd> <dt>

**Nem todas as concessões DHCP puderam ser liberadas/renovadas**
</dt> <dd>

98

</dd> <dt>

**DHCP não habilitado no adaptador**
</dt> <dd>

100

</dd> <dt>

**Outras**
</dt> <dd>

101 4294967295

</dd> </dl>

## <a name="remarks"></a>Comentários

Esse método só funciona quando a placa de interface de rede (NIC) está no modo de IP estático.

Para limpar o gateway, defina seu gateway para o mesmo IP usado em [**EnableStatic**](enablestatic-method-in-class-win32-networkadapterconfiguration.md).

## <a name="examples"></a>Exemplos

O exemplo de VBScript [modificar os gateways para um adaptador de rede](https://Gallery.TechNet.Microsoft.Com/9ea7670b-f68f-4efb-9cd2-7c299a8f657f) configura dois gateways para um adaptador de rede.

O exemplo [atribuir um endereço IP estático](https://Gallery.TechNet.Microsoft.Com/8979c752-8288-4a18-b5ed-f3b79f013f4a) VBScript define o endereço IP e o gateway de um computador.

O [IP estático e, em seguida, ingressar em um domínio](https://Gallery.TechNet.Microsoft.Com/Static-IP-and-then-join-to-130d4b8a) do PowerShell de exemplo ajuda na recriação de computadores.

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

 

