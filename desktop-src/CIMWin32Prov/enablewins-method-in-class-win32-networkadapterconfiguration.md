---
description: O &EnableWINS \# 32; O método estático de classe WMI Windows configurações wins (Internet Serviço de Nomenclatura) específicas para TCP/IP, mas independentes do adaptador de rede.
ms.assetid: ce0fb170-978f-4d70-bced-e530e43da719
ms.tgt_platform: multiple
title: Método EnableWINS da Win32_NetworkAdapterConfiguration classe
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_NetworkAdapterConfiguration.EnableWINS
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 1ce820e515bb72cbd2521521726f2b6962c49ee1b453781b5d17993c45e0d22d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118676499"
---
# <a name="enablewins-method-of-the-win32_networkadapterconfiguration-class"></a>Método EnableWINS da classe \_ NetworkAdapterConfiguration do Win32

O método estático da classe [WMI](/windows/desktop/WmiSdk/retrieving-a-class) **EnableWINS** habilita Windows configurações wins (Internet Serviço de Nomenclatura) específicas ao TCP/IP, mas independentemente do adaptador de rede.

Este tópico usa sintaxe Managed Object Format (MOF). Para obter mais informações sobre como usar esse método, consulte [Chamando um método](/windows/desktop/WmiSdk/calling-a-method).

## <a name="syntax"></a>Sintaxe


```mof
uint32 EnableWINS(
  [in]           boolean DNSEnabledForWINSResolution,
  [in]           boolean WINSEnableLMHostsLookup,
  [in, optional] string  WINSHostLookupFile,
  [in, optional] string  WINSScopeID
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*DNSEnabledForWINSResolution* \[ Em\]
</dt> <dd>

Se **for true,** o DNS (Sistema de Nomes de Domínio) será habilitado para resolução de nomes na resolução WINS.

</dd> <dt>

*WINSEnableLMHostsLookup* \[ Em\]
</dt> <dd>

Se **true**, os arquivos de lookup locais serão usados. Os arquivos de busca conterão mapeamentos de endereços IP para nomes de host.

</dd> <dt>

*WINSHostLookupFile* \[ in, opcional\]
</dt> <dd>

Arquivos de busca que contêm mapeamentos de endereços IP para nomes de host. Se disponível, os arquivos serão encontrados em %SystemRoot% \\ system32 \\ drivers \\ .

</dd> <dt>

*WINSScopeID* \[ in, opcional\]
</dt> <dd>

Valor do identificador de escopo que será anexado ao final do nome NetBIOS do computador. Sistemas que usam o mesmo identificador de escopo podem se comunicar com este computador.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Retorna um valor de 0 (zero) para uma conclusão bem-sucedida quando nenhuma reinicialização é necessária; 1 (um) para uma conclusão bem-sucedida quando uma reinicialização é necessária; um número diferente se houver um erro. Para obter mais informações sobre códigos de erro, consulte [**Constantes de erro WMI**](/windows/desktop/WmiSdk/wmi-error-constants) ou [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum). Para valores **gerais de HRESULT,** consulte [Códigos de erro do sistema.](/windows/desktop/Debug/system-error-codes)

<dl> <dt>

**Conclusão bem-sucedida, sem reinicialização** necessária (0)
</dt> <dt>

**Conclusão bem-sucedida, reinicialização necessária** (1)
</dt> <dt>

**Método sem suporte nesta plataforma** (64)
</dt> <dt>

**Falha desconhecida** (65)
</dt> <dt>

**Máscara de sub-rede inválida** (66)
</dt> <dt>

**Ocorreu um erro ao processar uma Instância que foi retornada** (67)
</dt> <dt>

**Parâmetro de entrada inválido** (68)
</dt> <dt>

**Mais de 5 gateways especificados** (69)
</dt> <dt>

**Endereço IP inválido** (70)
</dt> <dt>

**Endereço IP do gateway inválido** (71)
</dt> <dt>

**Ocorreu um erro ao acessar o Registro para as informações solicitadas** (72)
</dt> <dt>

**Nome de domínio inválido** (73)
</dt> <dt>

**Nome de host inválido** (74)
</dt> <dt>

**Nenhum servidor WINS primário/secundário definido** (75)
</dt> <dt>

**Arquivo inválido** (76)
</dt> <dt>

**Caminho do sistema inválido** (77)
</dt> <dt>

**Falha na cópia do** arquivo (78)
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

**Memória sem memória** (92)
</dt> <dt>

**Já existe** (93)
</dt> <dt>

**Caminho, arquivo ou objeto não encontrado** (94)
</dt> <dt>

**Não é possível notificar o** serviço (95)
</dt> <dt>

**Não é possível notificar o serviço DNS** (96)
</dt> <dt>

**Interface não configurável** (97)
</dt> <dt>

**Nem todas as concessões DHCP podem ser liberadas/renovadas** (98)
</dt> <dt>

**DHCP não habilitado no adaptador** (100)
</dt> <dt>

**Outros** (101 4294967295)
</dt> </dl>

## <a name="examples"></a>Exemplos

O exemplo de código Habilitar [WINS para](https://Gallery.TechNet.Microsoft.Com/64cae6dd-4155-4825-ab25-5727503edf5a) Todos os Adaptadores de Rede VBScript, na Galeria do TechNet, usa **EnableWINS** para Habilitar WINS em todos os adaptadores de rede instalados em um computador.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Vista<br/>                                                                |
| Servidor mínimo com suporte<br/> | Windows Server 2008<br/>                                                          |
| Namespace<br/>                | RAIZ \\ CIMV2<br/>                                                                  |
| MOF<br/>                      | <dl> <dt>CIMWin32.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>CIMWin32.dll</dt> </dl> |



## <a name="see-also"></a>Consulte também

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

 

