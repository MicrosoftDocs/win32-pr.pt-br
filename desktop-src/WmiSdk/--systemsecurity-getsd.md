---
description: Obtém o descritor de segurança para o namespace ao qual o usuário está conectado. Esse método retorna um descritor de segurança em formato de matriz de bytes binários. Se você estiver escrevendo um script, use o método GetSecurityDescriptor.
ms.assetid: aeac1e7b-fcb8-4880-afd1-4950da37602b
ms.tgt_platform: multiple
title: Método obtido da classe __SystemSecurity
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- __SystemSecurity.GetSD
api_type:
- COM
api_location:
- All
ms.openlocfilehash: 720443358cfce776dfe02630ea25ea994ad0ef552a9d89627b2f136e990e0194
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118109984"
---
# <a name="getsd-method-of-the-__systemsecurity-class"></a>Método obtido da \_ \_ classe SystemSecurity

O método **Extornado** Obtém o descritor de segurança para o namespace ao qual o usuário está conectado. Esse método retorna um descritor de segurança em formato de matriz de bytes binários. Se você estiver escrevendo um script, use o método [**GetSecurityDescriptor**](getsecuritydescriptor-method-in-class---systemsecurity-.md) . Para obter mais informações, consulte [protegendo os namespaces do WMI](securing-wmi-namespaces.md) e [alterando a segurança de acesso em objetos protegíveis](changing-access-security-on-securable-objects.md).

O usuário deve ter a **permissão \_ controle de leitura** . Por padrão, os administradores têm essa permissão. A única parte do descritor de segurança que é realmente usada é a DACL (lista de controle de acesso discricionário). A DACL pode conter ACEs herdadas e não herdadas. As ACEs Deny e Allow são permitidas.

Se você estiver programando em C++, poderá manipular o descritor de segurança binário usando [SDDL](/windows/desktop/SecAuthZ/security-descriptor-definition-language)e os métodos de conversão [**ConvertSecurityDescriptorToStringSecurityDescriptor**](/windows/desktop/api/sddl/nf-sddl-convertsecuritydescriptortostringsecuritydescriptora) e [**ConvertStringSecurityDescriptorToSecurityDescriptor**](/windows/desktop/api/sddl/nf-sddl-convertstringsecuritydescriptortosecuritydescriptora).

## <a name="syntax"></a>Sintaxe


```mof
HRESULT GetSD(
  [out] uint8 SD[]
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*SD* \[ fora\]
</dt> <dd>

Descritor de segurança em formato de matriz de bytes binários.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Esse método retorna um **HRESULT** que indica o status da chamada do método. A lista a seguir lista os valores de retorno que são de significância a serem **obtidas**. para aplicativos de script e Visual Basic, o resultado pode ser obtido de [parameters. ReturnValue](parsing-outparameters-objects.md). Para obter mais informações, consulte [construindo objetos de inparâmetros e analisando objetos de Parameters](constructing-inparameters-objects-and-parsing-outparameters-objects.md).

<dl> <dt>

**S \_ OK**
</dt> <dd>

Método executado com êxito.

</dd> <dt>

**acesso ao WBEM \_ E \_ \_ negado**
</dt> <dd>

O chamador não tem direitos suficientes para chamar este método.

</dd> <dt>

**\_método WBEM \_ E \_ desabilitado**
</dt> <dd>

Tentativa de executar este método em um sistema sem suporte.

</dd> </dl>

## <a name="remarks"></a>Comentários

Para obter mais informações sobre como modificar a segurança do namespace de forma programática ou manual, consulte [protegendo os namespaces do WMI](securing-wmi-namespaces.md).

## <a name="examples"></a>Exemplos

O script a seguir mostra como usar o **obtémd** para obter o descritor de segurança atual para o \\ namespace raiz Cimv2 e alterá-lo para a matriz de bytes mostrada em **exibido**.


```VB
Set objServices = GetObject("winmgmts:root\cimv2")
Set CimV2 = objServices.Get("__SystemSecurity=@")
ReturnValue = Cimv2.GetSD(arrSD)

If Err <> 0 Then
   WScript.Echo "Method returned error " & ReturnValue
End If

DisplaySD = "SD = {"
For I = Lbound(arrSD) To Ubound(arrSD)

   DisplaySD = DisplaySD & arrSD(I)

   If I <> Ubound(arrSD) Then
      DisplaySD = DisplaySD & ","
   End If

Next

DisplaySD = DisplaySD & "}"

WScript.Echo DisplaySD
```



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|--------------------------------|
| Cliente mínimo com suporte<br/> | Windows Vista<br/>       |
| Servidor mínimo com suporte<br/> | Windows Server 2008<br/> |
| Namespace<br/>                | Todos os namespaces do WMI<br/>  |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Classes do sistema WMI](wmi-system-classes.md)
</dt> <dt>

[**\_\_SystemSecurity**](--systemsecurity.md)
</dt> <dt>

[Constantes de segurança do WMI](wmi-security-constants.md)
</dt> <dt>

[**Ace do Win32 \_**](/previous-versions/windows/desktop/secrcw32prov/win32-ace)
</dt> <dt>

[**\_\_SystemSecurity:: definido**](--systemsecurity-setsd.md)
</dt> <dt>

[**\_Descritor de segurança**](/windows/desktop/api/winnt/ns-winnt-security_descriptor)
</dt> <dt>

[**\_SecurityDescriptor Win32**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor)
</dt> <dt>

[Protegendo namespaces WMI](securing-wmi-namespaces.md)
</dt> </dl>

 

