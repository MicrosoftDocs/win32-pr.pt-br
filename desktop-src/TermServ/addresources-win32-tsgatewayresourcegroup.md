---
title: Método Resources da classe Win32_TSGatewayResourceGroup
description: Adiciona recursos ao grupo de recursos.
ms.assetid: 3210b468-6b82-4edb-ac8b-95f66a7b9328
ms.tgt_platform: multiple
keywords:
- Serviços de Área de Trabalho Remota do método addresources
- Método addresources Serviços de Área de Trabalho Remota, classe Win32_TSGatewayResourceGroup
- Classe Win32_TSGatewayResourceGroup Serviços de Área de Trabalho Remota, método addresources
topic_type:
- apiref
api_name:
- Win32_TSGatewayResourceGroup.AddResources
api_location:
- AagWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a37498accf76b28f16e0de45565916c18ab8d9dc
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104499269"
---
# <a name="addresources-method-of-the-win32_tsgatewayresourcegroup-class"></a>Método Resources da \_ classe Win32 TSGatewayResourceGroup

Adiciona recursos ao grupo de recursos.

## <a name="syntax"></a>Sintaxe


```mof
uint32 AddResources(
  [in] string Resources
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*Recursos* \[ do no\]
</dt> <dd>

Lista separada por ponto e vírgula de recursos a serem adicionados ao grupo de recursos. Um " \* " significa todos os recursos.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Se o método tiver sucesso, ele retornará zero. Se o método não for bem-sucedido, ele retornará um valor diferente de zero. Para obter uma lista de códigos de erro, consulte [serviços de área de trabalho remota códigos de erro do provedor WMI](terminal-services-wmi-provider-error-codes.md).

## <a name="remarks"></a>Comentários

Se vários recursos estiverem no parâmetro de *recursos* e um dos recursos não puder ser processado, nenhum dos recursos será processado.

Você deve ser um membro do grupo Administradores para chamar esse método.

Os arquivos de formato MOF (MOF) contêm as definições de classes de Instrumentação de Gerenciamento do Windows (WMI). Os arquivos MOF não são instalados como parte do SDK (Software Development Kit) do Microsoft Windows. Eles são instalados no servidor quando você adiciona a função associada usando o Gerenciador do Servidor. Para obter mais informações sobre arquivos MOF, consulte [formato MOF (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).

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

 

