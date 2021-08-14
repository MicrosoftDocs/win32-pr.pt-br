---
title: Método Resources da classe Win32_TSGatewayResourceGroup
description: Define a propriedade Resources para esse grupo de recursos.
ms.assetid: 0043ee04-26d1-4907-87cc-a15f72cb0b93
ms.tgt_platform: multiple
keywords:
- Método Resources serviços de área de trabalho remota
- Método Resources serviços de área de trabalho remota, classe Win32_TSGatewayResourceGroup
- Classe Win32_TSGatewayResourceGroup serviços de área de trabalho remota, método Resources
topic_type:
- apiref
api_name:
- Win32_TSGatewayResourceGroup.SetResources
api_location:
- AagWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 77f357b08e554c5fa97cc26d15c52e65a0668512eeef20bceeba8d194510bdf0
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119987666"
---
# <a name="setresources-method-of-the-win32_tsgatewayresourcegroup-class"></a>Método Resources da \_ classe Win32 TSGatewayResourceGroup

Define a propriedade **Resources** para esse grupo de recursos.

## <a name="syntax"></a>Sintaxe


```mof
uint32 SetResources(
  [in] string Resources
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*Recursos* \[ do no\]
</dt> <dd>

Lista de recursos separados por ponto e vírgula neste grupo de recursos. Um " \* " significa todos os recursos.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Se o método tiver sucesso, ele retornará zero. Se o método não for bem-sucedido, ele retornará um valor diferente de zero. Para obter uma lista de códigos de erro, consulte [serviços de área de trabalho remota códigos de erro do provedor WMI](terminal-services-wmi-provider-error-codes.md).

## <a name="remarks"></a>Comentários

Se vários recursos estiverem no parâmetro de *recursos* e um dos recursos não puder ser processado, nenhum dos recursos será processado.

Você deve ser um membro do grupo Administradores para chamar esse método.

os arquivos de formato MOF (MOF) contêm as definições de classes de Instrumentação de Gerenciamento do Windows (WMI). os arquivos MOF não são instalados como parte do SDK (Software Development Kit) do Microsoft Windows. Eles são instalados no servidor quando você adiciona a função associada usando o Gerenciador do Servidor. Para obter mais informações sobre arquivos MOF, consulte [formato MOF (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Nenhum compatível<br/>                                                                |
| Servidor mínimo com suporte<br/> | Windows Server 2008<br/>                                                           |
| Namespace<br/>                | \\TerminalServices da CIMv2 raiz \\<br/>                                                 |
| MOF<br/>                      | <dl> <dt>TS. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>AagWmi.dll</dt> </dl>    |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**\_TSGatewayResourceGroup Win32**](win32-tsgatewayresourcegroup.md)
</dt> </dl>

 

