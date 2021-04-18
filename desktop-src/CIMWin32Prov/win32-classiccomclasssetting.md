---
description: Representa as configurações de um componente de Component Object Model (COM).
ms.assetid: 18d9ddf2-184d-4680-8d56-f012c608ff7d
ms.tgt_platform: multiple
title: Classe Win32_ClassicCOMClassSetting
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_ClassicCOMClassSetting
- Win32_ClassicCOMClassSetting.Caption
- Win32_ClassicCOMClassSetting.Description
- Win32_ClassicCOMClassSetting.SettingID
- Win32_ClassicCOMClassSetting.AppID
- Win32_ClassicCOMClassSetting.AutoConvertToClsid
- Win32_ClassicCOMClassSetting.AutoTreatAsClsid
- Win32_ClassicCOMClassSetting.ComponentId
- Win32_ClassicCOMClassSetting.Control
- Win32_ClassicCOMClassSetting.DefaultIcon
- Win32_ClassicCOMClassSetting.InprocHandler
- Win32_ClassicCOMClassSetting.InprocHandler32
- Win32_ClassicCOMClassSetting.InprocServer
- Win32_ClassicCOMClassSetting.InprocServer32
- Win32_ClassicCOMClassSetting.Insertable
- Win32_ClassicCOMClassSetting.JavaClass
- Win32_ClassicCOMClassSetting.LocalServer
- Win32_ClassicCOMClassSetting.LocalServer32
- Win32_ClassicCOMClassSetting.LongDisplayName
- Win32_ClassicCOMClassSetting.ProgId
- Win32_ClassicCOMClassSetting.ShortDisplayName
- Win32_ClassicCOMClassSetting.ThreadingModel
- Win32_ClassicCOMClassSetting.ToolBoxBitmap32
- Win32_ClassicCOMClassSetting.TreatAsClsid
- Win32_ClassicCOMClassSetting.TypeLibraryId
- Win32_ClassicCOMClassSetting.Version
- Win32_ClassicCOMClassSetting.VersionIndependentProgId
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 5f263a888ce9dea80444023faff57998bc3f2c1c
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105771698"
---
# <a name="win32_classiccomclasssetting-class"></a>\_Classe Win32 ClassicCOMClassSetting

A [classe WMI](/windows/desktop/WmiSdk/retrieving-a-class) **\_ ClassicCOMClassSetting do Win32** representa as configurações de um componente com (Component Object Model).

A sintaxe a seguir é simplificada do código MOF (Managed Object Format) e inclui todas as propriedades herdadas. As propriedades são listadas em ordem alfabética, não em ordem MOF.

## <a name="syntax"></a>Sintaxe

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{E5D8A562-F6C0-11d2-B35E-00105A1F8569}"), AMENDMENT]
class Win32_ClassicCOMClassSetting : Win32_COMSetting
{
  string  Caption;
  string  Description;
  string  SettingID;
  string  AppID;
  string  AutoConvertToClsid;
  string  AutoTreatAsClsid;
  string  ComponentId;
  boolean Control;
  string  DefaultIcon;
  string  InprocHandler;
  string  InprocHandler32;
  string  InprocServer;
  string  InprocServer32;
  boolean Insertable;
  boolean JavaClass;
  string  LocalServer;
  string  LocalServer32;
  string  LongDisplayName;
  string  ProgId;
  string  ShortDisplayName;
  string  ThreadingModel;
  string  ToolBoxBitmap32;
  string  TreatAsClsid;
  string  TypeLibraryId;
  string  Version;
  string  VersionIndependentProgId;
};
```

## <a name="members"></a>Membros

A classe **Win32 \_ ClassicCOMClassSetting** tem estes tipos de membros:

-   [Propriedades](#properties)

### <a name="properties"></a>Propriedades

A classe **Win32 \_ ClassicCOMClassSetting** tem essas propriedades.

<dl> <dt>

**AppID**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry \| HKEY \_ local \_ Machine \\ \\ software \\ \\ classes \\ \\ CLSID \\ \\ {GUID} \[ AppID \] ")
</dt> </dl>

GUID (identificador global exclusivo) para o aplicativo COM usando este componente COM.

</dd> <dt>

**AutoConvertToClsid**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry \| HKEY \_ local \_ Machine \\ \\ software \\ \\ classes \\ \\ CLSID \\ \\ {GUID} \\ \\ conversão Autoconverter em \[ padrão \] ")
</dt> </dl>

GUID da classe COM na qual esse componente COM será automaticamente convertido.

</dd> <dt>

**AutoTreatAsClsid**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry \| HKEY \_ local \_ Machine \\ \\ software \\ \\ classes \\ \\ CLSID \\ \\ {GUID} \\ \\ autotratáas \[ padrão \] ")
</dt> </dl>

GUID do componente COM que emulará automaticamente as instâncias dessa classe.

</dd> <dt>

**Legenda**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)
</dt> </dl>

Breve descrição textual do objeto atual.

Essa propriedade é herdada [**da \_ configuração de CIM**](cim-setting.md).

</dd> <dt>

**ComponentId**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**chave**](/windows/desktop/WmiSdk/key-qualifier), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry \| HKEY \_ local \_ Machine \\ \\ software \\ \\ classes \\ \\ CLSID \\ \\ {GUID} \[ padrão \] ")
</dt> </dl>

GUID deste componente COM.

</dd> <dt>

**Controle**
</dt> <dd> <dl> <dt>

Tipo de dados: **booliano**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry \| HKEY \_ local \_ Machine \\ \\ software \\ \\ classes \\ \\ CLSID \\ \\ {GUID} \\ \\ controle")
</dt> </dl>

O componente COM é um controle OLE.

</dd> <dt>

**DefaultIcon**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry \| HKEY \_ local \_ Machine \\ \\ software \\ \\ classes \\ \\ CLSID \\ \\ {GUID} \\ \\ DefaultIcon \[ padrão \] ")
</dt> </dl>

Caminho para o arquivo executável e o identificador de recurso do ícone padrão usado pela classe.

</dd> <dt>

**Descrição**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Descrição textual do objeto atual.

Essa propriedade é herdada [**da \_ configuração de CIM**](cim-setting.md).

</dd> <dt>

**InprocHandler**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry \| HKEY \_ local \_ Machine \\ \\ software \\ \\ classes \\ \\ CLSID \\ \\ {GUID} \\ \\ InprocHandler \[ padrão \] ")
</dt> </dl>

Caminho completo incluindo nome de arquivo ou somente nome de arquivo para um manipulador personalizado de 16 bits para o componente COM. O provedor nem sempre retorna o caminho completo.

</dd> <dt>

**InprocHandler32**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry \| HKEY \_ local \_ Machine \\ \\ software \\ \\ classes \\ \\ CLSID \\ \\ {GUID} \\ \\ InprocHandler32 \[ padrão \] ")
</dt> </dl>

Caminho completo incluindo nome de arquivo ou somente nome de arquivo para um manipulador personalizado de 32 bits para o componente COM. O provedor nem sempre retorna o caminho completo.

</dd> <dt>

**InprocServer**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry \| HKEY \_ local \_ Machine \\ \\ software \\ \\ classes \\ \\ CLSID \\ \\ {GUID} \\ \\ InprocServer \[ padrão \] ")
</dt> </dl>

Caminho completo incluindo nome de arquivo ou somente nome de arquivo para uma DLL de servidor em processo de 16 bits para este componente COM. O provedor nem sempre retorna o caminho completo.

</dd> <dt>

**InprocServer32**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry \| HKEY \_ local \_ Machine \\ \\ software \\ \\ classes \\ \\ CLSID \\ \\ {GUID} \\ \\ InprocServer32 \[ padrão \] ")
</dt> </dl>

Caminho completo incluindo nome de arquivo ou somente nome de arquivo para uma DLL de servidor em processo de 32 bits para este componente COM. O provedor nem sempre retorna o caminho completo.

</dd> <dt>

**Insertable**
</dt> <dd> <dl> <dt>

Tipo de dados: **booliano**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry \| HKEY \_ local \_ Machine \\ \\ software \\ \\ classes \\ \\ CLSID \\ \\ {GUID} \\ \\ Insertable")
</dt> </dl>

O componente COM pode ser inserido em aplicativos de contêiner OLE.

</dd> <dt>

**JavaClass**
</dt> <dd> <dl> <dt>

Tipo de dados: **booliano**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry \| HKEY \_ local \_ Machine \\ \\ software \\ \\ classes \\ \\ CLSID \\ \\ {GUID} \\ \\ InprocServer32 \[ JavaClass \] ")
</dt> </dl>

O componente COM é um componente Java.

</dd> <dt>

**LocalServer**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry \| HKEY \_ local \_ Machine \\ \\ software \\ \\ classes \\ \\ CLSID \\ \\ {GUID} \\ \\ LocalServer \[ padrão \] ")
</dt> </dl>

Caminho completo incluindo nome de arquivo ou somente nome de arquivo para um aplicativo de servidor local de 16 bits. O provedor nem sempre retorna o caminho completo.

</dd> <dt>

**LocalServer32**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry \| HKEY \_ local \_ Machine \\ \\ software \\ \\ classes \\ \\ CLSID \\ \\ {GUID} \\ \\ LocalServer32 \[ padrão \] ")
</dt> </dl>

Caminho completo incluindo nome de arquivo ou somente nome de arquivo para um aplicativo de servidor local de 32 bits. O provedor nem sempre retorna o caminho completo.

</dd> <dt>

**LongDisplayName**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry \| HKEY \_ local \_ Machine \\ \\ software \\ \\ classes \\ \\ CLSID \\ \\ {GUID} \\ \\ AuxUserType \\ \\ 3 \[ padrão \] ")
</dt> </dl>

Nome completo do aplicativo COM. Ele é usado em áreas como o campo **resultados** da caixa de diálogo de **colar especial do OLE** .

</dd> <dt>

**ProgId**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry \| HKEY \_ local \_ Machine \\ \\ software \\ \\ classes \\ \\ CLSID \\ \\ {GUID} \\ \\ ProgID \[ padrão \] ")
</dt> </dl>

Identificador programático associado ao componente COM. O formato de um ProgID é <<Component. <versão. Não há garantia de que esse identificador seja exclusivo.

</dd> <dt>

**SettingID**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)
</dt> </dl>

Identificador pelo qual o objeto atual é conhecido.

Essa propriedade é herdada [**da \_ configuração de CIM**](cim-setting.md).

</dd> <dt>

**ShortDisplayName**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry \| HKEY \_ local \_ Machine \\ \\ software \\ \\ classes \\ \\ CLSID \\ \\ {GUID} \\ \\ AuxUserType \\ \\ 2 \[ padrão \] ")
</dt> </dl>

Nome curto do aplicativo COM (usado em menus e pop-ups).

</dd> <dt>

**ThreadingModel**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry \| HKEY \_ local \_ Machine \\ \\ software \\ \\ classes \\ \\ CLSID \\ \\ {GUID} \\ \\ InprocServer32 \[ ThreadingModel \] ")
</dt> </dl>

Modelo de Threading usado por classes COM em processo. Se essa propriedade for **nula**, nenhum modelo de Threading será usado. O componente é criado no thread principal do cliente e as chamadas de outros threads são empacotadas para esse thread.

O modelo de apartamento especifica que os componentes podem ser inseridos por um e apenas um thread. Os dados comuns mantidos por esses tipos de servidores de objetos devem ser protegidos contra colisões de thread porque o servidor de objetos dá suporte a vários componentes. Cada componente pode ser inserido simultaneamente por threads diferentes.

O modelo gratuito especifica que os componentes não colocam restrições em quais threads ou quantos threads podem inserir o objeto. O objeto não pode conter dados específicos de thread e deve proteger seus dados de acesso simultâneo por vários threads. No entanto, os componentes de thread livre não podem ser acessados por threads de apartamento diretamente e as chamadas para eles são empacotadas no apartamento do cliente.

Quando ambos são especificados, os componentes podem ser usados nos modos Apartment-Threaded ou Free-threaded. Esses componentes podem ser inseridos por vários threads, proteger seus dados de colisões de thread e não conter dados específicos de thread.

Os valores são:

<dl> <dd>Sta</dd> <dd>Informações</dd> <dd>Mesmo</dd> </dl>

<dt>

<span id="Apartment"></span><span id="apartment"></span><span id="APARTMENT"></span>

**Apartamento** ("Apartment")


</dt> <dd></dd> <dt>

<span id="Free"></span><span id="free"></span><span id="FREE"></span>

**Gratuito** ("gratuito")


</dt> <dd></dd> <dt>

<span id="Both"></span><span id="both"></span><span id="BOTH"></span>

**Ambos** ("both")


</dt> <dd></dd> </dl>

</dd> <dt>

**ToolBoxBitmap32**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry \| HKEY \_ local \_ Machine \\ \\ software \\ \\ classes \\ \\ CLSID \\ \\ {GUID} \\ \\ ToolBoxBitmap32 \[ padrão \] ")
</dt> </dl>

O nome do módulo e o identificador de recurso para um pequeno bitmap (16x16) usado para a face de uma barra de ferramentas ou botão de caixa de ferramentas. Usado quando o componente COM é um controle OLE ou ActiveX.

</dd> <dt>

**TreatAsClsid**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry \| HKEY \_ local \_ Machine \\ \\ software \\ \\ classes \\ \\ CLSID \\ \\ {GUID} \\ \\ trata de \[ padrão \] ")
</dt> </dl>

GUID de um componente COM que pode emular instâncias desse componente.

</dd> <dt>

**TypeLibraryId**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry \| HKEY \_ local \_ Machine \\ \\ software \\ \\ classes \\ \\ CLSID \\ \\ {GUID} \\ \\ TypeLib \[ padrão \] ")
</dt> </dl>

GUID da biblioteca de tipos para este componente COM.

</dd> <dt>

**Versão**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry \| HKEY \_ local \_ Machine \\ \\ software \\ \\ classes \\ \\ CLSID \\ \\ {GUID} \\ \\ versão \[ padrão \] ")
</dt> </dl>

Número de versão desta classe COM.

</dd> <dt>

**VersionIndependentProgId**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry \| HKEY \_ local \_ Machine \\ \\ software \\ \\ classes \\ \\ CLSID \\ \\ {GUID} \\ \\ VersionIndependentProgId \[ padrão \] ")
</dt> </dl>

Identificador de programa consistente para todas as versões do mesmo programa.

</dd> </dl>

## <a name="remarks"></a>Comentários

A classe **Win32 \_ ClassicCOMClassSetting** é derivada da [**\_ configuração do Win32**](win32-comsetting.md).

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

[**Configuração do Win32 \_**](win32-comsetting.md)
</dt> <dt>

[Classes do sistema operacional](/previous-versions//aa392727(v=vs.85))
</dt> </dl>

 

